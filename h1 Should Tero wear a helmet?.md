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

## Data Flow Diagrams (DFDs) are commonly used to visualize the system.
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
