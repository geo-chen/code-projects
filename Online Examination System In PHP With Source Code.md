# Online Examination System In PHP With Source Code


[Online Examination System In PHP With Source Code](https://code-projects.org/online-examination-system-in-php-with-source-code-2/) is a popular Examination CMS released in January 2026. 

Within 3 days of its release, the open-source project has been downloaded more than 15k times:
<img width="1119" height="304" alt="image" src="https://github.com/user-attachments/assets/8fc0df89-fb33-4596-94d8-7a09f5fec17f" />

This exercise is jointly run with @JoshuaSim24.

### Finding 1: Stored XSS in all "add" pages

Multiple XSS vulnerabilities were found in the following forms:

 - /onexam/add_visitor.php
 - /onexam/add_offering.php
 - /onexam/add_teen.php (on practically all available fields)
 - /onexam/admin_user.php (on practically all available fields)

Screenshots:
| ![](https://github.com/user-attachments/assets/67de6e00-6ccb-479a-aba3-ed09b461f051) | ![](https://github.com/user-attachments/assets/8df1b8e4-bd29-4695-8025-9abefc93348d) | ![](https://github.com/user-attachments/assets/e01e282e-7b99-42d6-81a4-37c79820ae32) |
|---|---|---|
| ![](https://github.com/user-attachments/assets/6aaa9bbe-3f9e-48b3-86e0-8d7c063006f7) | ![](https://github.com/user-attachments/assets/10f90c46-3e7b-4736-af36-9777bef0639d) | ![](https://github.com/user-attachments/assets/ff01c8be-50cf-4e59-a704-14654e89c698) |


### Finding 2: SQL Injection on Login Page

The insecure usage of "mysql_*", which is deprecated, is used across the project. Here's a sample endpoint where an sqli gets you logged into the admin account (muler, by default):

 - /onexam/index.php

![2026-01-13 00-10-20](https://github.com/user-attachments/assets/ddab7ee9-38f6-4e9c-9579-692cde9dd887)


### Finding 3: Remote Code Execution via Unsafe File Upload

The "Change Picture" feature invokes "/onexam/admin_pic.php" to replace the logo for the website, but does not restrict on file types. As a result, an attacker can upload a php webshell and gain remote code execution:

![2026-01-13 00-10-20 (2)](https://github.com/user-attachments/assets/c3854391-61bf-4bc8-b249-5ae8d5a45c7e)

![2026-01-13 00-10-20 (3)](https://github.com/user-attachments/assets/26693f5c-3af0-4283-95dd-dc9e89682ea1)

