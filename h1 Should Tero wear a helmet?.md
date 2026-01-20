# Braiterman et al 2020: threat modeling menifesto:

## What is Threat Modeling?

Threat modeling is the process of analyzing a system to identify security and privacy risks. It helps understand how a system works and where it might be vulnerable to threats.

## Key Questions in Threat Modeling

+ What system are we working on?
+ What can go wrong?
+ What actions can we take to reduce or mitigate risks?
+ Have we done enough to address the identified threats?

## Why Threat Modeling is Important?

+ Helps identify security and privacy issues early in the system lifecycle.
+ Supports better design and implementation decisions.
+ Threats identified guide development, testing and post-deployment improvements.
+ Encourages continuous security improvement.

## Using the Threat Modeling Manifesto

+ Acts as a guiding framework rather than a step-by-step method.
+ Can be adapted to fit different organizational needs.
+ Focuses on effectiveness rather than tools or rigid processes.
+ Inspired by the Agile Manifesto.

# Shostack 2022: Worlds shortest threat modeling video

The videos explain that threat modeling is a simple but powerful way to improve system security by thinking about problems early.
Threat modeling is based on four simple questions:
+ What are we working on?
  * Collaboration is important.
  * Tools like whiteboards, online drawing or sketching helps turn ideas from our heads into something others can understand and later can be changed easily.
+ What could go wrong?
  * Structure can help when people are unsure how to answer.
  * Frameworks like STRIDE can improve consistency.
+ What are we going to do about it?
  * Every identified threat must be handled.
  * Adding operational controls to handel the threat
  * Not to ignore or forget threats.
+ Did we do a good job?
  * A simple way to evaluate success is to ask colleague "Would they recommend threat modeling".
  * If the answer is yes, the process was likely valuable.
  * If the answer is no, improvements are needed.

# OWASP CheatSheets Series Team 2021: threat modeling cheat sheet

## Threat Modeling advantages

+ Helps identify security risks before the system is built.
+ Improves security awareness by encouraging teams.
+ Helps teams better understand data flows, trust boundaries and system interactions.

## What Are We Building?

Data Flow Diagrams (DFDs) are commonly used to visualize the system.
+ Five elements of DFDs:
  * External entities.
  * Processes
  * Data flows
  * Data stores
  * Trust boundaries
+ Whiteboards can also be effective, especially for teamwork.
+ Brainstorming helps improve communication and shared understanding, even for non-technical participants.

## Cloud Threat Modeling

+ Many modern systems are cloud-based or hybrid.
+ Cloud threat modeling must consider:
  * Shared responsibility between cloud provider and customer
  * Managed services and APIs
  * Identity and access management
  * Dynamic infrastructure (IaC, serverless, containers)
+ Cloud frameworks like AWS Well-Architected Framework can be helpful references.

## What Can Go Wrong?

+ After modeling the system, threats are identified.
+ STRIDE is a widely used framework for threat identification.
  * Spoofing – breaking authentication
  * Tampering – affecting data integrity
  * Repudiation – manipulates logs to cover their actions.
  * Information disclosure – data leaks
  * Denial of service – affecting availability
  * Elevation of privilege – gaining unauthorized access.

## Responses and Mitigations

Once threats are identified, actions must be taken:
+ Mitigate – reduce the risk
+ Eliminate – remove the risky feature
+ Transfer – shift responsibility
+ Accept – accept the risk due to business reasons

## Review and Validation

+ The threat model should be reviewed by all stakeholders.
+ Documentation is important for future reference and audits.

## Challenges for Development Teams

+ Lack of security knowledge among developers.
+ Threat modeling can be time-consuming.
+ Poor communication between security and development teams.
+ Limited tools and resources.

## To Address These Challenges

+ Involve security experts in threat modeling sessions
+ Provide regular security training for developers
+ Use tools that simplify and automate threat modeling.

# Darkest Daires Podcast: EP 113: Adam

## Adam’s background:
+ Grew up bullied and unprotected in Australia as a result lost trust in police after failed intervention.
+ Joined a gang for protection and belonging, which led to crime and prison.
+ Moved to the UK for a fresh start and tried to rebuild his life through IT work.

## First IT job at the School Academy:
+ Adam worked as an IT apprentice at a private high school.
+ Discovering his criminal record through a background check, the school later terminated his employment.
+ Felt betrayed and angry, despite trying to change his life.

## Major security weaknesses at the Academy:

+ Same local admin password used across all computers.
+ Password patterns were predictable.
+ Reused across multiple systems.
+ Never changed after Adam left.

## Unauthorized access 4 years later:

+ Adam logged into the school’s Office 365 using old-valid admin credentials.
+ Read emails, monitored alerts and avoided detection initially.
+ Escalated access by changing a super admin password.
+ Adam found VPN credentials, moved across servers, backups and domain controls.

## Destructive actions:

+ Deleted user accounts and infrastructure.
+ Remotely wiped nearly 3,000 mobile devices including students, staff and parents.
+ A complete shutdown of the school’s digital operations.
+ Caused total system outage during COVID remote learning.
+ School's financial losses were significant and some data was permanently lost.

## Police investigation and arrest:

+ Adam was traced through his IP address.
+ Adam cooperated fully and confessed.
+ He explained how he accessed the systems, what accounts he used and what actions he took.

## Second attack on another employer:

+ Adam had attacked another employer after being fired.
+ This time he had a disagreement about using the companies credit card.
+ He changed passwords and disrupted systems as revenge.
+ Arrested again and charged from both cases were combined.

## Court Case sentencing and consequences:

+ In February 2022, Adam was sentenced to 21 months in prison.
+ His IT career was effectively destroyed

## Main lesson:

+ Organizations must change admin passwords immediately when staff leave.
+ Least privilege and strong password policies are critical.
+ Personal anger and poor emotional control can destroy lives.

## What basic security practices should everyone follow? Are there some security hygiene practicies that every company or average Joe should follow?

IT security includes different practices and tools that help protect systems, networks and data from unauthorized access and attacks. Here are some best practices for IT Security:
+ Regularly update and patch your software and systems:
  * Keep operating systems, applications and firmware up to date.
  * Apply security patches promptly to fix known vulnerabilities.
  * Update third-party software such as browsers, plugins, and antivirus tools.
+ Use Strong and Unique Passwords:
  * Create passwords with a mix of uppercase, lowercase, numbers, and symbols.
  * Avoid same password everywhere, common words, personal information, and predictable patterns.
  * Use unique passwords for different accounts.
  * Change passwords regularly.
+ Enable Multi-Factor Authentication:
  * Require more than one authentication factor
  * Use MFA for email, cloud services, banking, and administrative accounts.
  * Reduce the risk of unauthorized access significantly.
+ Educate Employees on IT Security:
  * Training employees on password hygiene, phishing awareness and safe browsing.
  * Teach employees to recognize suspicious emails and links.
  * Conduct regular security awareness training.
  * Traning for handling sensitive data.
  * Encourage reporting of suspicious activities or security incidents.
+ Regularly Backup and Encrypt Data:
  * Perform regular backups to prevent data loss.
  * Store backups securely, preferably off-site or in the cloud.
  * Ensure backups are tested and recoverable.
+ Monitor and Detect Security Threats:
  * Continuously monitor systems, networks, and user activity.
  * Review logs and security alerts regularly.
  * Detect insider threats using user behavior analytics (UBA).
+ Conduct Security Audits and Vulnerability Assessments:
  * Perform regular security audits to evaluate controls and policies.
  * Identify gaps in access control, encryption and system configurations.
  * vulnerability assessments to identifying potential weaknesses in the system.
  * Prioritize and address vulnerabilities before they can be exploited and reducing the risk of a security breach (it-pillars, 2025).

# Threat Model for an Imaginary Company – PhonePay

## Business description and goal:

PhonePay is a Finland based company offering a mobile wallet application for customers across the European Union.The service enables users to store money, make fast peer-to-peer (P2P) transfers, pay merchants online and in-store with linking their EU bank accounts. Revenue is generated through transaction fees, merchant fees and premium user accounts.

## Business Narrative:

+ Business stakeholders define requirements such as customer trust, low transaction friction and high availability.
+ Technical specialists design and operate the mobile app, backend systems, APIs and security controls that implement these requirements.
+ Security supports the business by protecting money and identities, ensuring uninterrupted payment services and maintaining trust so customers continue using PhonePay.

## 4 Threat modeling manifesto

## 1) What are we working on?

This frist step of threat modeling is about clearly understanding the system before thinking about attacks. In other words, What exactly are we trying to protect and why does it matter to the business? Business Assest are identified based on how important they are to the business.
+ High-value assets:
  * Customer funds stored in PhonePay wallets
  * Correctness and integrity of transactions
  * Customer authentication credentials
  * User personal information or KYC data
  * Linked bank account information
  * Payment and transaction logs
  * Customer trust and PhonePay brand reputation
+ Lower-valued assets:
  * PhonePay wallets internal dashboards
  * Marketing website content

 ## Customer Perspective

From the customer’s point of view, PhonePay is mainly used through the mobile app. Customers expect the app to be simple, fast and always available.
+ Customer touchpoints:
  * Mobile application (iOS and Android)
  * Push notifications and email receipts
  * Customer support portal
+ From the customer’s perspective, PhonePay must:
  * Always be available when payments are needed
  * Protect money and personal data
  * Process transactions accurately and instantly
To continue receiving revenue, PhonePay must ensure that payments work reliably and securely all times.

## Company systems diagram
This system diagram represents what must function correctly in order for PhonePay to serve customers and get paid.
Customer ---> Mobile App ---> API Gateway ---> Authentication Service ---> Wallet Service ---> Transaction Database ---> Banking API Gateway | Encrypted Backups | Admin Console ---> Monitoring, Logs, Fraud Detection

## 2) What Can Go Wrong?

This step is about thinking like an attacker and like the business at the same time. If we run PhonePay, what bad things could happen to our system, our customers and our business. So, STRIDE helps to ask six simple questions that help to analyse problems can happen.
Threat Modeling Method STRIDE Analysis:
+ Spoofing: An attacker gains access to a user account using stolen credential
+ Tampering: Manipulation of transaction amounts.
+ Repudiation: Insufficient logging makes it difficult to prove who initiated a transaction.
+ Information Disclosure: Leakage of customer personal information or transaction data.
+ Denial of Service: An attack prevents users from making payments.
+ Elevation of Privilege: An attacker gains administrative access to backend systems.

## High-Risk Prioritization

+ Account takeover fraud ---> Medium Probability ---> 30,00,000$ (Very High Impact)
+ Payment system outage (1 day) ---> medium Probability ---> 10,00,000$ (High Impact)
+ KYC data breach ---> Low–Medium Probability ---> 25,00,000$ (Very High Impact)

## Threat Actors and Targeting

Companies like PhonePay are primary targets for cybercriminals because they handle money.
+ Organized cybercriminal groups
+ Malicious insiders or competitors
+ Scammers pretends to be service provider

## COI assessment

The COI model helps to determine the "behavior" of an attacker, which is directly influenced by the combination of these three factors.
+ Capability: High, due to widely available attack tools.
+ Opportunity: High, because the system requires internet to run.
+ Intent: High, driven by direct financial gain

## Business Continuity and Trust

PhonePay must remain operational to continue earning revenue. Even short outages or security incidents can significantly damage customer trust, which is difficult to rebuild.

## 3) What Are We Going To Do About It?

This step is about deciding what PhonePay will actually do in response to the risks identified. This treatment decisions are made jointly by business and technical teams.

## Risk Treatment (META)

+ Mitigating threats:
  * Multi-factor authentication for users and administrators
  * Encryption of sensitive data
  * Fraud detection and monitoring
+ Eliminating threats:
  * Remove unused services and APIs
  * Avoid storing unnecessary sensitive data
+ Transferring threats:
  * Cyber insurance for fraud and scame
  * Use regulated banking partners to hold funds
+ Accepting threats:
  * Limited downtime during planned maintenance
These measures aim to reduce the likelihood and impact of the most important risks while supporting business goals.

## 4) Did We Do a Good Enough Job?

This final stage of the process is simply about continually improving out threat modelling processes, which is not a one time activity but an ongoing process.

+ Evaluation and Improvement:
  * Monthly internal and external security audits
  * Penetration testing of the mobile app and APIs
  * Continuous monitoring and alerting
  * Incident response quickly
+ Continuous Threat Modeling:
  * Update based on new threat intelligence
  * Reassess risks based on emerging fraud techniques
  * lessons learned from incidents
This threat model demonstrates how security supports PhonePay’s business by protecting customer funds, ensuring availability and maintaining trust.

# References




