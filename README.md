# spring-security-csrf

There is inconsistent response between Spring Boot 2.7.x and 3.0.x when the CSRF protection is enabled and the CSRF token is missing.

    # @no-redirect
    POST http://localhost:8080/login
    Content-Type: application/x-www-form-urlencoded
    
    username=admin&password=hardPassword

In Spring Boot 2.7.5 it responds with 403
In Spring Boot 3.0.2 it responds with 302 /login

For some reason SecurityApplicationTests gives same response for both versions of Spring Boot.

youtube video https://youtu.be/K4mYYQUWE9s
