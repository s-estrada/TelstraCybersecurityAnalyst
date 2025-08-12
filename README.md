# Telstra Cybersecurity Virtual Experience Repository
- https://www.telstra.com.au/
- https://www.theforage.com/virtual-internships/prototype/RNhbu8QnDzthwynEf/Cybersecurity?ref=NatiJPDMj6TPQBjeC

This repository documents the work completed during the Telstra Cybersecurity Virtual Experience, focusing on the role of a cybersecurity analyst. The program simulates a real-world scenario involving a malware attack and is structured around four key tasks.

### Task 1: Responding to a Malware Attack
This section covers the initial stages of a malware attack, including the immediate response and triaging of security alerts. The work demonstrates skills in incident detection, response coordination, and effective communication with various teams.

### Task 2: Analyzing the Attack
This task involves a detailed analysis of the malware attack to understand its propagation methods and behavioral patterns. The repository showcases proficiency in network analysis, data analysis, and threat research.

### Task 3: (Technical) Mitigating the Malware Attack

This part focuses on the technical mitigation of the attack. It includes the development and implementation of firewall rules using Python to block the malware's identified network patterns. The task highlights skills in security engineering, software development, and problem-solving.

## Task 4: Incident Postmortem
The final task is a comprehensive post-incident review. This section includes a detailed postmortem report that reflects on the incident's timeline, impact, root cause, and resolution, and outlines a strategy for future improvements. It emphasizes skills in root cause analysis, governance, and risk management.

This repository provides solutions, code samples, and example communications to illustrate the skills and knowledge acquired through the Telstra Cybersecurity Virtual Experience.


# In-Depth Task Descriptions

## Task 1 (T1): Incident Initiation - Awareness and Mitigation
This task centers on the initial incident response. The goal is to triage malware threats, identify compromised infrastructure, and dispatch an initial incident communication to the relevant teams, providing awareness and mitigation steps to begin the response process.

Background Information:
You are an information security analyst in the Security Operations Centre. A common task and responsibility of information security analysts in the SOC is to respond to triage incoming threats and respond appropriately, by notifying the correct team depending on the severity of the threat. It’s important to be able to communicate the severity of the incident to the right person so that the organisation can come together in times of attack. The firewall logs & list of infrastructure has been provided, which shows critical services that run the Spring Framework and need to be online / uninterrupted. A list of teams has also been provided, which depending on the severity of the threat, must be contacted. It’s important to note that the service is down and functionality is impaired due to the malware attack.

Task:
Your task is to triage the current malware threat and figure out which infrastructure is affected. First, find out which key infrastructure is currently under attack. Note the priority of the affected infrastructure to the company - this will determine who is the respective team to notify. After, draft an email to the respective team alerting them of the current attack so that they can begin an incident response. Make sure to include the timestamp of when the incident occurred. Make it concise and contextual. The purpose of this email is to ensure the respective team is aware of the ongoing incident and to be prepared for mitigation advice.

[CVE Websites](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/Task%201%20CVE%20Websites)

[Firewall Infrastructure](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/Task%201_2%20-%20Firewall_Infrastructure%20List.xlsx)

[Email Template](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T1%20-%20Email%20Template.docx)

## Task 2 (T2): Firewall Rule Creation Request
This task involves analyzing firewall logs to identify attacker network patterns. The deliverable is a formal request to the firewall management team, detailing the attack, specifying the traffic to be blocked, and providing supporting research findings.

## Task 3 (T3) - Firewall Server
This part of the repository contains the solution for a custom firewall server developed in Python. The server is designed to inspect incoming HTTP requests for malicious headers and block those that match a predefined list. The core functionality is implemented using Python's http.server module, extending BaseHTTPRequestHandler to perform header analysis and send a 403 Forbidden response for malicious requests.

Usage:

git clone https://github.com/track001/TelstraCybersecurityAnalyst.git

cd TelstraCybersecurityAnalyst

python main.py

The server runs on localhost at port 8000.

Task 4: Postmortem Report
This section includes a comprehensive postmortem report for the Spring4Shell malware incident. The report details the incident from detection to resolution, providing a structured analysis of its impact, root cause, and the steps taken to contain and mitigate the attack. It concludes with actionable items to prevent future occurrences. The report is organized into the following sections:

Summary: An overview of the incident, including its timeline, severity, and key stakeholders.

Impact: An assessment of the potential consequences, such as data exfiltration or system disruption.

Detection: An explanation of how the attack was discovered through proactive monitoring and threat detection systems.

Root Cause: A deep-dive into the underlying vulnerability (Spring4Shell) that was exploited.

Resolution: A summary of the immediate actions taken, including system isolation, firewall rule implementation, and patching.

Action Items: A list of recommendations to enhance security posture, such as vulnerability assessments and security awareness training.

ACSC Essential Eight Mitigation Strategies
These are a set of Australian Cyber Security Centre (ACSC) recommended strategies to bolster system security against various cyber threats.  They include:

Application Control: Limiting software execution to an approved list.

Patching: Regularly updating applications and operating systems to address vulnerabilities.

User Application Hardening: Securing applications like web browsers and Office suites.

Restricting Admin Privileges: Limiting administrative access to minimize the blast radius of an attack.

Backups: Performing regular data backups for effective disaster recovery.
