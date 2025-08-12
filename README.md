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

### Task 4: Incident Postmortem
The final task is a comprehensive post-incident review. This section includes a detailed postmortem report that reflects on the incident's timeline, impact, root cause, and resolution, and outlines a strategy for future improvements. It emphasizes skills in root cause analysis, governance, and risk management.

This repository provides solutions, code samples, and example communications to illustrate the skills and knowledge acquired through the Telstra Cybersecurity Virtual Experience.


# In-Depth Task Descriptions

## Task 1 (T1): Incident Initiation - Awareness and Mitigation
This task centers on the initial incident response. The goal is to triage malware threats, identify compromised infrastructure, and dispatch an initial incident communication to the relevant teams, providing awareness and mitigation steps to begin the response process.

Background Information:
You are an information security analyst in the Security Operations Centre. A common task and responsibility of information security analysts in the SOC is to respond to triage incoming threats and respond appropriately, by notifying the correct team depending on the severity of the threat. It’s important to be able to communicate the severity of the incident to the right person so that the organisation can come together in times of attack. The firewall logs & list of infrastructure has been provided, which shows critical services that run the Spring Framework and need to be online / uninterrupted. A list of teams has also been provided, which depending on the severity of the threat, must be contacted. It’s important to note that the service is down and functionality is impaired due to the malware attack.

Task:
Your task is to triage the current malware threat and figure out which infrastructure is affected. First, find out which key infrastructure is currently under attack. Note the priority of the affected infrastructure to the company - this will determine who is the respective team to notify. After, draft an email to the respective team alerting them of the current attack so that they can begin an incident response. Make sure to include the timestamp of when the incident occurred. Make it concise and contextual. The purpose of this email is to ensure the respective team is aware of the ongoing incident and to be prepared for mitigation advice.

### Task 1 Resources:
- [CVE Websites](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/Task%201%20CVE%20Websites)
- [Firewall Infrastructure](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/Task%201_2%20-%20Firewall_Infrastructure%20List.xlsx)
- [Email Template](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T1%20-%20Email%20Template.docx)

## Task 2 (T2): Firewall Rule Creation Request
This task involves analyzing firewall logs to identify attacker network patterns. The deliverable is a formal request to the firewall management team, detailing the attack, specifying the traffic to be blocked, and providing supporting research findings.

## Task 3 (T3) - Firewall Server
This part of the repository contains the solution for a custom firewall server developed in Python. The server is designed to inspect incoming HTTP requests for malicious headers and block those that match a predefined list. The core functionality is implemented using Python's http.server module, extending BaseHTTPRequestHandler to perform header analysis and send a 403 Forbidden response for malicious requests.

## Usage

1. Clone the repository to your local machine:

```shell
git clone https://github.com/track001/TelstraCybersecurityAnalyst.git
```

### Navigate to the cloned repository:
```shell
cd <TelstraCybersecurityAnalyst>
```
Run the Firewall Server:
```shell
python main.py
```
The Firewall Server will start running on localhost at port 8000.

## Explanation
The Firewall Server code is implemented using Python's built-in http.server module. It extends the BaseHTTPRequestHandler class to handle incoming requests and perform header analysis.

The `block_request` function handles blocking a request and sending a 403 Forbidden response.

The `handle_request` function processes each incoming request. It checks the request path and examines the request headers for potential malicious headers. If a request is on the Spring Framework path and contains any of the predefined bad headers, the request is blocked and a 403 Forbidden response is sent.

The ServerHandler class defines the behavior for different HTTP methods (GET and POST). It calls the handle_request function to process incoming requests.

## Task 4 (T4) - Postmortem
This repository contains the postmortem report for the Spring4Shell malware attack incident. The postmortem provides a detailed analysis of the incident, including its impact, detection, root cause, resolution, and action items for future improvement.

The Spring4Shell malware attack targeted the Spring Framework within our system infrastructure. The incident was promptly detected and addressed by the Security Operations Center (SOC) team. This postmortem report outlines the key findings and actions taken to mitigate the attack.

### Contents
- Summary
- Impact
- Detection
- Root Cause
- Resolution
- Action Items

### Summary
The Spring4Shell malware attack involved the exploitation of a vulnerability in the Spring Framework, allowing unauthorized code execution and potential system compromise. This section provides a summary of the incident, including timestamps, severity, and key stakeholders involved.

### Impact
The impact section describes the potential consequences of the malware attack, including unauthorized access, data theft, and system disruption. It highlights the measures taken to mitigate the impact and protect sensitive data.

### Detection
The detection section explains how the malware attack was discovered, including the proactive monitoring and anomaly detection systems that triggered alerts. It provides insights into the network traffic patterns and malicious HTTP headers associated with the Spring4Shell vulnerability.

### Root Cause
The root cause analysis identifies the underlying cause of the incident, which was the presence of the Spring4Shell vulnerability in our system. It describes the vulnerability and its impact on the affected systems.

### Resolution
The resolution section outlines the immediate actions taken to contain and mitigate the malware attack. It includes details on isolating the affected system, implementing firewall rules, and patching/updating the Spring Framework to secure versions.

### Action Items
The action items section provides a list of recommended steps and measures to prevent similar incidents in the future. It covers areas such as vulnerability assessment, intrusion detection, system monitoring, and security awareness training.

---

By conducting this postmortem and implementing the recommended action items, we aim to strengthen our system security, minimize the risk of future incidents, and ensure the ongoing protection of our infrastructure and data.

# ACSC 8 Mitigation Strategies 
ACSC 8 essential mitigation strategies are a set of recommended cybersecurity practices to make it harder for adversaries to compromise systems. 

[Get the Basics of Cyber Security Right: The Essential Eight](https://www.telstra.com.au/smarter-business/cyber-security-and-safety/how-to-get-the-basics-of-cyber-security-right)


These strategies are:

- Application Control: Ensuring only approved applications can be installed or executed on systems.
- Patch Applications: Upgrading software to the latest versions to fix known vulnerabilities.
- Configure Microsoft Office Macro settings: Securing Microsoft Office applications by managing macro settings.
- User Application Hardening: Configuring and updating applications to work securely.
- Restrict Administrative privileges: Limiting administrative privileges to minimize the risk of unauthorized access.
- Patch Operating Systems: Keeping operating systems up to date with the latest patches.
- Regular Backups: Performing regular backups to protect data and enable recovery in case of an incident.
