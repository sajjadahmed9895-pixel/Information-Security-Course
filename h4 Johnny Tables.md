# What is OWASP Top 10?

The OWASP Top 10 is a list created by the Open Web Application Security Project (OWASP). It identifies the most critical security risks in web applications. From my understanding, the OWASP Top 10 acts like a guideline showing where developers most often make mistakes and how attackers exploit them.

# A01:2021 — Broken Access Control

Broken access control is one of the most common and critical web application vulnerabilities according to OWASP Top 10 (2021).Access control is supposed to enforce rules so that users only access resources allowed for their roles. When this fails, attackers may view sensitive data, modify information, or perform privileged actions.

## Common Problems

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

# A05:2021 — Security Misconfiguration

Security misconfiguration has become one of the most common web application risks in the OWASP Top 10.Security misconfiguration happens when systems, applications, or services are not securely configured or hardened properly.

## Common Causes

+ Missing security hardening across servers, cloud services, or application components.
+ Unnecessary features enabled (unused ports, services, accounts, or privileges).
+ Default accounts or passwords still active.
+ Error messages exposing technical details or stack traces.
+ Security features disabled after system upgrades.
+ Application frameworks, databases, or servers using insecure default settings.

## Prevention Methods

+ Use secure installation and configuration processes.
+ Apply a repeatable hardening process for development, QA, and production environments.
+ Remove unnecessary features and unused components.
+ Regularly review configurations and apply patches.
+ Secure cloud permissions and storage settings.

# A06:2021 — Vulnerable and Outdated Components

Vulnerable and outdated components is also a major security risk identified in OWASP Top 10. Many organizations struggle to assess this risk because modern applications rely heavily on third-party components and nested dependencies. If these components are not maintained or updated, attackers can exploit publicly known vulnerabilities.

## Common Causes

+ Developers do not know all component versions being used.
+ Software components or systems are outdated or unsupported (including OS, database, APIs, libraries).
+ Vulnerability scanning is not performed regularly.
+ Security patches are delayed or not applied on time.
+ Compatibility testing is not done after updates.
+ Component configurations are not secured properly.

  ## Prevention Methods

  + Maintain a proper patch management process.
  + Remove unused dependencies and unnecessary features.
  + Keep an updated inventory of all components and versions.
  + Monitor CVE and security vulnerability databases.
  + Download components only from official trusted sources.
  + Maintain continuous update and monitoring processes during the application lifecycle.

  # A03:2021 — Injection

Injection is ranked as one of the most critical vulnerabilities in the OWASP Top 10. Injection vulnerabilities occur when an application processes untrusted user input as part of commands or queries without proper validation or protection.

## Common Causes

+ User input is not properly validated or sanitized.
+ Dynamic queries are built without parameterized statements.
+ User data is directly concatenated into SQL or commands.
+ ORM queries accept unsafe parameters.
+ Applications accept hostile input through URLs, headers, cookies, JSON, XML, or APIs.

## Prevention Methods

+ Use parameterized queries or safe APIs.
+ Separate user input from commands and queries.
+ Apply server-side input validation.
+ Escape special characters when dynamic queries are unavoidable.
+ Avoid allowing users to define database structures like table or column names.

# Install WebGoat 2023.4

+ First I checked java is installad or not so I found it was not. So then installed it with these command "sudo apt-get update" then "sudo apt-get install openjdk-17-jre"
+ To keep safe, I should have a firewall. So I installed that too.
+ Before downloaded the  WebGoat JAR file i had to installed wget in my linux platfrom by this command "sudo apt install wget".
+ Then I ran this command to download this file "wget https://github.com/WebGoat/WebGoat/releases/download/v2023.4/webgoat-2023.4.jar".
+ At some point it told you go on a platfrom http://127.0.0.1:8888/WebGoat where i had to creat user id to enter the WebGoat platfrom.
+ So I created a ID for me and it looks like this:
![WhatsApp Image 2026-02-08 at 8 41 50 PM](https://github.com/user-attachments/assets/9a92e2eb-47fc-4392-a901-0e55942e3761)

# Developer Tools Exercise

+ In this exercise, browser developer tools were used to inspect the webpage structure and analyze hidden elements. By opening the developer tools with F12, it was possible to view HTML elements, hidden fields, and network requests. There was couple of wanrings in the console pannel.

![WhatsApp Image 2026-02-08 at 8 50 16 PM](https://github.com/user-attachments/assets/3c10806f-4b8a-4db0-9671-49389e6dd7a5)


  


