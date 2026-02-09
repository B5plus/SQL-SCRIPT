&P1_FULL_NAME.

&P1_DEPARTMENT.

&P1_STATUS.

&P1_ROLE_CNT.

&P1_ACCESS_CNT.

&P1_MODULE_CNT.

&P1_JOINED.

&P1_ROLE_ROWS.

&P1_UPDATE_ROWS.

&P1_LAST_ROLE_DATE.





SET_HOME_VALUES


declare
  l_user_id   number := to_number(apex_util.get_session_state('APP_CURRENT_USER_ID'));
  l_is_admin  number := 0;
begin
  /* 1) USER INFO */
  select u.full_name,
         u.department,
         u.status,
         to_char(u.created_at, 'DD-MON-YYYY')
    into :P1_FULL_NAME,
         :P1_DEPARTMENT,
         :P1_STATUS,
         :P1_JOINED
    from app_users u
   where u.user_id = l_user_id;

  /* 2) ROLE COUNT + LAST ROLE ASSIGNED DATE */
  select count(*),
         max(nvl(ur.assigned_at, ur.created_at))
    into :P1_ROLE_CNT,
         :P1_LAST_ROLE_DATE
    from app_user_roles ur
   where ur.user_id = l_user_id;

  /* Convert date to readable text (if exists) */
  :P1_LAST_ROLE_DATE :=
    case
      when :P1_LAST_ROLE_DATE is not null
      then to_char(to_date(:P1_LAST_ROLE_DATE), 'DD-MON-YYYY')
      else null
    end;

  /* 3) ACCESS COUNT (page access) */
  select count(*)
    into :P1_ACCESS_CNT
    from app_user_page_access a
   where a.user_id = l_user_id;

  /* 4) MODULE COUNT (distinct modules from pages user can access)
        - Admin (role_id=1) sees all active pages
        - normal user sees only granted pages
  */
  select case
           when exists (select 1 from app_user_roles r where r.user_id = l_user_id and r.role_id = 1)
           then 1 else 0
         end
    into l_is_admin
    from dual;

  if l_is_admin = 1 then
    select count(distinct p.module_name)
      into :P1_MODULE_CNT
      from app_pages p
     where p.status = 'ACTIVE';
  else
    select count(distinct p.module_name)
      into :P1_MODULE_CNT
      from app_user_page_access a
      join app_pages p on p.page_id = a.page_id
     where a.user_id = l_user_id
       and p.status = 'ACTIVE';
  end if;

  /* 5) ROLE ROWS (HTML) */
  :P1_ROLE_ROWS := null;

  for r in (
    select ro.role_name,
           ro.description
      from app_user_roles ur
      join app_roles ro on ro.role_id = ur.role_id
     where ur.user_id = l_user_id
     order by ro.role_name
  ) loop
    :P1_ROLE_ROWS :=
      :P1_ROLE_ROWS ||
      '<div class="b5row">'||
        '<div class="b5row__title">'||apex_escape.html(r.role_name)||'</div>'||
        '<div class="b5row__sub">'||apex_escape.html(nvl(r.description,'-'))||'</div>'||
      '</div>';
  end loop;

  if :P1_ROLE_ROWS is null then
    :P1_ROLE_ROWS := '<div class="b5empty">No roles assigned yet.</div>';
  end if;

  /* 6) UPDATE ROWS (HTML)
        If you have an audit table use it.
        If not, we show a simple placeholder block.
  */
  :P1_UPDATE_ROWS :=
    '<div class="b5empty">No recent updates yet.</div>';

exception
  when no_data_found then
    :P1_FULL_NAME := 'User';
    :P1_DEPARTMENT := '-';
    :P1_STATUS := '-';
    :P1_ROLE_CNT := 0;
    :P1_ACCESS_CNT := 0;
    :P1_MODULE_CNT := 0;
    :P1_JOINED := '-';
    :P1_ROLE_ROWS := '<div class="b5empty">No roles found.</div>';
    :P1_UPDATE_ROWS := '<div class="b5empty">No updates.</div>';
    :P1_LAST_ROLE_DATE := null;
end;
