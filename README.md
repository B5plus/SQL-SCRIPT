DECLARE
  l_user_id  app_users.user_id%TYPE;
  l_now      DATE := SYSDATE;
  l_count    NUMBER;
BEGIN
  -- 1) get user_id from email
  SELECT user_id
    INTO l_user_id
    FROM app_users
   WHERE upper(username) = upper(:P102_EMAIL);

  -- 2) validate otp (not used + not expired)
  SELECT COUNT(*)
    INTO l_count
    FROM app_user_otp
   WHERE user_id    = l_user_id
     AND otp_code   = :P102_OTP
     AND used_flag  = 'N'
     AND expires_at >= l_now;

  IF l_count = 0 THEN
    apex_error.add_error(
      p_message          => 'Invalid or expired OTP.',
      p_display_location => apex_error.c_inline_in_notification
    );
    RETURN;
  END IF;

  -- 3) mark used
  UPDATE app_user_otp
     SET used_flag = 'Y'
   WHERE user_id   = l_user_id
     AND otp_code  = :P102_OTP
     AND used_flag = 'N';

  -- 4) set session state (THIS makes RBAC menu work)
  apex_util.set_session_state('APP_CURRENT_USER_ID', l_user_id);
  apex_util.set_session_state('APP_CURRENT_USER_EMAIL', :P102_EMAIL);

  COMMIT;

  -- 5) redirect to HOME
  APEX_UTIL.REDIRECT_URL('f?p=' || :APP_ID || ':1:' || :APP_SESSION);
  apex_application.stop_apex_engine;

EXCEPTION
  WHEN NO_DATA_FOUND THEN
    apex_error.add_error(
      p_message          => 'Unknown user.',
      p_display_location => apex_error.c_inline_in_notification
    );
END;
