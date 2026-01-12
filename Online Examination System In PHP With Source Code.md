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

### Finding 2: 
