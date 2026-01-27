# Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains

+ This article explains how cyber defenders can fight advanced attackers by breaking attacks into stages (kill chain) and using intelligence from past attacks to stop future ones.
+ Basically, it explains why traditional cybersecurity defenses (antivirus, IDS, patching, incident response) are not sufficient against Advanced Persistent Threats (APTs), which are skilled, well-funded and long-term attackers.
+ APTs usually target sensitive information (government, military, intellectual property) and use custom tools, social engineering, and zero-day exploits, allowing them to bypass common security controls.
+ The authors propose an intelligence-driven computer network defense (CND) approach, which focuses on understanding the adversary, their behavior, tools and campaigns, not only technical vulnerabilities.
+ The main contribution of the paper is the Intrusion Kill Chain model, which breaks cyber attacks into seven stages:
  * Reconnaissance – researching and selecting targets.
  * Weaponization – preparing malware and exploit.
  * Delivery – sending weapon (email, website, USB, etc.)
  * Exploitation – triggering vulnerability or user action.
  * Installation – installing backdoor/malware.
  * Command & Control (C2) – attacker communicates with victim system.
  * Actions on Objectives – data theft, sabotage, or lateral movement
+ The key idea is that an attack can be stopped at any stage. If defenders disrupt just one phase, the entire intrusion can fail.
+ The paper introduces the concept of indicators (atomic, computed and behavioral) and explains their life cycle, showing how defenders can collect, mature, and reuse intelligence from past attacks.
+ A courses of action matrix maps different defensive actions (detect, deny, disrupt, degrade, deceive, destroy) to each stage of the kill chain, helping organizations plan layered and resilient security controls.
+ The authors emphasize campaign analysis, where multiple intrusions are linked over time to identify attacker patterns, tools, and techniques (TTPs). This allows defenders to predict and block future attacks.
+ A real case study from 2009 shows how Lockheed Martin detected several targeted email attacks and was able to stop a later attack using a previously unknown zero-day exploit by relying on intelligence from earlier actions.

## My own Insight 

+ This paper made me realize that cybersecurity defense is not only a technical issue, but also an intelligence and learning process where organizations must continuously study attacker behavior.
+ An important insight from this paper is that even very advanced attackers can be weakened if defenders systematically analyze and learn from previous attacks.

## My Question

+ How realistic it is for small or resource-limited organizations to build and maintain this level of intelligence-driven defense compared to large organizations like Lockheed Martin?.
+ If attackers keep changing their tools and methods or technique, does that make them harder for defenders to recognize and track?

# Tactics, tools and procedures

## Define tactic and give an example of a specific tactic.

+ A tactic represents the attacker’s objective or goal at a particular stage of an intrusion. It answers the question: Why is the adversary performing this action?
+ Tactics describe what the attacker is trying to achieve, such as gaining initial access, maintaining persistence, escalating privileges, or stealing data.
+ Example of a tactic:
  * Credential Access: The attacker’s goal is to steal usernames and passwords.

## Define technique and subtechnique, and give an example of each.

+ Technique: A technique explains how an attacker achieves a tactical goal. It is a general method used to carry out part of an attack.
+ Example of a technique:
  * Phishing: The attacker sends a fake email to trick users into giving their login details.
+ Subtechnique: A sub-technique is a more specific way of performing a technique. It breaks a technique into cleae and more detailed behaviors.
+ Example of a subtechnique:
  * Spearphishing Attachment: The attacker sends a fake email with a malicious Word or PDF file attached.

## Define procedure, and give an example of each.

+ A procedure is the exact real-world way an attacker carries out a technique or sub-technique.
+ It includes the specific tools, commands, scripts, or malware used by attackers.
+ Example of a procedure:
  * The attacker sends an email that looks like it came from Microsoft Support with a file called “Password_Reset.docx”.
  * When the victim opens it, the file asks them to enter their email and password, which are then sent to the attacker.
