#Telstra Cybersecurity Virtual Experience Repository
This repository documents the work completed during the Telstra Cybersecurity Virtual Experience, focusing on the role of a cybersecurity analyst. The program simulates a real-world scenario involving a malware attack and is structured around four key tasks.

Task 1: Incident Response & Triage
This section covers the initial stages of a malware attack, including the immediate response and triaging of security alerts. The work demonstrates skills in incident detection, response coordination, and effective communication with various teams.

Task 2: Attack Analysis
This task involves a detailed analysis of the malware attack to understand its propagation methods and behavioral patterns. The repository showcases proficiency in network analysis, data analysis, and threat research.

Task 3: Malware Mitigation (Technical)
This part focuses on the technical mitigation of the attack. It includes the development and implementation of firewall rules using Python to block the malware's identified network patterns. The task highlights skills in security engineering, software development, and problem-solving.

Task 4: Incident Postmortem
The final task is a comprehensive post-incident review. This section includes a detailed postmortem report that reflects on the incident's timeline, impact, root cause, and resolution, and outlines a strategy for future improvements. It emphasizes skills in root cause analysis, governance, and risk management.

This repository provides solutions, code samples, and example communications to illustrate the skills and knowledge acquired through the Telstra Cybersecurity Virtual Experience.

In-Depth Task Descriptions
Task 1: Incident Initiation - Awareness and Mitigation
This task centers on the initial incident response. The goal is to triage malware threats, identify compromised infrastructure, and dispatch an initial incident communication to the relevant teams, providing awareness and mitigation steps to begin the response process.

Task 2: Firewall Rule Creation Request
This task involves analyzing firewall logs to identify attacker network patterns. The deliverable is a formal request to the firewall management team, detailing the attack, specifying the traffic to be blocked, and providing supporting research findings.

Task 3: Firewall Server (Python)
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
