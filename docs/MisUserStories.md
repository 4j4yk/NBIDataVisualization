# MisUser Stories

1. As a misuser, i should be able to perform brute force attack, so that i can access NBI data application.

   *Mitigation Criteria :* NBI data application authentication should follow secure and strong authentication mechanism, so that it can be                            acceptably secure from  the brute force attacks
   
2. As a misuser, i should be able to spoof the HTTP request data, so that i can get information required to access the NBI data              application.

   *Mitigation Criteria :* NBI data application should encrypt the HTTP traffic data using standard encryption method, so that it can                                avoid the attackers from spoofing.

3. As a misuser, i should be able to give input HTML that includes JavaScript into any input field, so that i can run my JavaScript code      in the web application.

  *Mitigation Criteria :* NBI data application should use automatic input sanitizers like Django-Bleach in the models, which will                                   automatically sanitize the HTML input and presents safe HTML to the application preventing XSS weaknesses. 
