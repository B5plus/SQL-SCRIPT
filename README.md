select *
from app_user_roles
where user_id = (select user_id from app_users where username = 'the_email_you_created');
