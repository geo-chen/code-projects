# Online Examination System In PHP With Source Code


[Online Examination System In PHP With Source Code](https://code-projects.org/online-examination-system-in-php-with-source-code-2/) is a popular Examination CMS released in January 2026. 

Within 3 days of its release, the open-source project has been downloaded more than 15k times:
<img width="1119" height="304" alt="image" src="https://github.com/user-attachments/assets/8fc0df89-fb33-4596-94d8-7a09f5fec17f" />

This exercise is jointly run by @JoshuaSim24 and Joseph.


### Finding 1: SQL Injection enabling access without proper credentials
<img width="2880" height="1749" alt="image" src="https://github.com/user-attachments/assets/0518e7cd-e40f-4292-bfb6-70ab003bb499" />
No proper checks in place to prevent basic SQL injection.
Using simple ' or '1'='1 allows people to gain access to the system.
Screenshot below showing access to admin portal
<img width="2871" height="1748" alt="image" src="https://github.com/user-attachments/assets/c3131d56-42ac-4369-a44b-24672ef55aa9" />

This also works for the student login portal - The error at the top appears to be a result of code error and not SQL injection (logging in properly via known credentials also displays the same error)
<img width="2879" height="1760" alt="image" src="https://github.com/user-attachments/assets/f6e1496b-9b60-47cf-b6e0-a46c5fdf09b0" />
