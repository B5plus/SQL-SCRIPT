SELECT FULL_NAME || ' (' || USERNAME || ')' AS display_value,
       USER_ID                         AS return_value
FROM   APP_USERS
WHERE  STATUS = 'ACTIVE'
ORDER  BY FULL_NAME;
