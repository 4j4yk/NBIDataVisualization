# NBI Data Visualization

## MisUser Stories

 1. As a misuser, i want to perform brute force attack, so that i can gain access to NBI data application.

   *Mitigation Criteria :* NBI data application authentication should disable the user on 3 consecutive failed login attempts.

 2. As a misuser, i want to sniff the HTTP traffic data, so that i can get information required to gain access to the NBI data application.

   *Mitigation Criteria :* NBI data application should encrypt the HTTP traffic data using standard encryption method, so that it can avoid the attackers from packet sniffing. For security, It is always recommended to deploy the web site behind HTTPS.

 3. As a misuser, i want to give input HTML that includes JavaScript into any input field, so that i can run my JavaScript code in the web application and gain control over the NBI data application.

   *Mitigation Criteria :* NBI data application should use automatic input sanitizer like Django-Bleach in the models, which will automatically sanitize the HTML input and presents safe HTML to the application preventing XSS weaknesses.

 4. As a misuser, i want to execute random SQL code using the input fields,  so that i can get required information from the database to gain access the NBI data application.

   *Mitigation Criteria :* NBI data application should properly escape the resulting SQL query and avoid any SQL injection attacks. By using Django's querysets, the SQL queries will be properly escaped by the database driver before the actual query execution on the database.
