---
layout: post
title:  "💉 Fun ways to learn SQL injection"
date:   2023-02-20 20:26:48 +0100
---

I spent several years specializing in software security for web applications. During that time, I worked on a side project where I created practical exercises to help students gain a better understanding of SQL injection and cultivate an interest in it. As I have invested more than 100 hours in research of learning materials, I thought it might be worth sharing a few.

## Security Idiots

[Security Idiots](https://www.securityidiots.com/) is a penetration testing blog. It has more than 30 posts [on SQL injection](https://www.securityidiots.com/Web-Pentest/SQL-Injection/#), covering different variants of the exploit.
A detailed walkthrough of simple variants makes it good for beginners, while the diversity of exploits makes it good for advanced students.

Unfortunatelly, the last blog post is from 2019, but all the content is still relevant.

![Security Idiots SQL injection page]({{site.url}}/assets/2023-02-19-sqli/security-idiots.png)

## Juice Shop

[Juice Shop](https://owasp.org/www-project-juice-shop/) is an open-source web application
representing an insecure online shop. The ever-growing popularity of e-commerce makes the domain quite relevant. 

It was created by OWASP
organization and contains 100 challenges of varying
difficulty where the user is supposed to exploit the underlying vulnerabilities.
SQL injection is covered by 7 of them.

![Juice Shop main page]({{site.url}}/assets/2023-02-19-sqli/juice-shop.png)

## Hack The Box

[Hack The Box](https://www.hackthebox.com/) is training platform
helping individuals, companies and universities improve
penetration testing skills. 

Exercises are updated daily and progress of the user is tracked and awarded with
points, ranks and badges. 

They are performed in a
realistic environment, for example, against a web
application instance.

It includes dedicated challenges for SQL injection, like [SQL Injection Fundamentals](https://academy.hackthebox.com/module/details/33) and a fresh drop - [Blind SQL Injection](https://academy.hackthebox.com/module/details/177).

Some of the web exercises require combining SQL injection with other exploits. 

![Hack The Box Dashboard]({{site.url}}/assets/2023-02-19-sqli/hack-the-box.png)

Thanks for reading! I hope you found this post helpful, interesting, or at least mildly amusing. If you have any feedback, questions, or funny cat videos to share, feel free to connect with me [on twitter](https://twitter.com/dmadic) and let me know. See you in the next post!