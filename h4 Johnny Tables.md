# What is OWASP Top 10?

The OWASP Top 10 is a list created by the Open Web Application Security Project (OWASP). It identifies the most critical security risks in web applications. From my understanding, the OWASP Top 10 acts like a guideline showing where developers most often make mistakes and how attackers exploit them.

# A01:2021 — Broken Access Control

Broken access control is one of the most common and critical web application vulnerabilities according to OWASP Top 10 (2021).Access control is supposed to enforce rules so that users only access resources allowed for their roles. When this fails, attackers may view sensitive data, modify information, or perform privileged actions.

## Common Problems (based on OWASP description)

+ Violating the principle of least privilege (users get more access than necessary).
+ Changing URL parameters or manipulating requests to bypass security checks.
+ Accessing other users’ data using IDs (Insecure Direct Object References).
+ APIs missing access control for methods like POST, PUT, DELETE.
+ Privilege escalation (normal user acting as admin).
+ Manipulating cookies, tokens, or JWT metadata.
+ CORS misconfiguration allowing unauthorized access.
+ Accessing restricted pages without authentication (force browsing).

## Prevention Methods

+ Enforce access control on server-side code.
+ Use deny-by-default strategy (only allow explicitly permitted actions).
+ Reuse centralized access control mechanisms.
+ Verify ownership of records before allowing actions.
+ Disable unnecessary directory listings or exposed files.
+ Log failed access attempts and monitor suspicious behavior.
+ Use rate limiting to reduce automated attacks.

# 
