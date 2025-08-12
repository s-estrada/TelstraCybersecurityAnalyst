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

### Background Information:
You are an information security analyst in the Security Operations Centre. A common task and responsibility of information security analysts in the SOC is to respond to triage incoming threats and respond appropriately, by notifying the correct team depending on the severity of the threat. It’s important to be able to communicate the severity of the incident to the right person so that the organisation can come together in times of attack. The firewall logs & list of infrastructure has been provided, which shows critical services that run the Spring Framework and need to be online / uninterrupted. A list of teams has also been provided, which depending on the severity of the threat, must be contacted. It’s important to note that the service is down and functionality is impaired due to the malware attack.

### Task:
Your task is to triage the current malware threat and figure out which infrastructure is affected. First, find out which key infrastructure is currently under attack. Note the priority of the affected infrastructure to the company - this will determine who is the respective team to notify. After, draft an email to the respective team alerting them of the current attack so that they can begin an incident response. Make sure to include the timestamp of when the incident occurred. Make it concise and contextual. The purpose of this email is to ensure the respective team is aware of the ongoing incident and to be prepared for mitigation advice.

### Task 1 Resources:
- [Firewall Infrastructure](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/Task%201_2%20-%20Firewall_Infrastructure%20List.xlsx)
- [Email Template](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T1%20-%20Email%20Template.docx)
- CVE Websites:
    [CISA Alert Advisory on Spring4Shell zero-day vulnerability](https://www.cisa.gov/news-events/alerts/2022/04/01/spring-releases-security-updates-addressing-spring4shell-and-spring-cloud-function-vulnerabilities) & [CVE Advisory on Spring4Shell zero-day vulnerability](https://spring.io/security/cve-2022-22965)

## Task 2 (T2): Firewall Rule Creation Request
This task involves analyzing firewall logs to identify attacker network patterns. The deliverable is a formal request to the firewall management team, detailing the attack, specifying the traffic to be blocked, and providing supporting research findings.

### Background Information:
Now that you have notified the infrastructure owner of the current attack, analyse the firewall logs to find the pattern in the attacker’s network requests. You won’t be able to simply block IP addresses, because of the distributed nature of the attack, but maybe there is another characteristic of the request that is easy to block. An important responsibility of an information security analyst is the ability to work across disciplines with multiple teams, both technical and non-technical. In the resources section, we have attached a proof of concept payload that may be of interest in understanding how the attacker scripted this attack.

### Task:
First, analyse the firewall logs in the resources section. Next, identify what characteristics of the Spring4Shell vulnerability have been used. Finally, draft an email to the networks team with your findings. Make sure to be concise, so that they can develop the firewall rule to mitigate the attack. You can assume the recipient is technical and has dealt with these types of requests before.

### Task 2 Resources:
- [Spring4Shell Proof of Concept Payload](https://github.com/craig/SpringCore0day/blob/main/exp.py)
- [Affected Infrastructure List & Firewall Logs](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T1%20-%20Firewall_Infrastructure%20List.xlsx)
- [Firewall Rule Creation Request Email Template](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T2%20-%20Firewall%20Request%20Template.docx)

## Task 3 (T3) - Firewall Server
This part of the repository contains the solution for a custom firewall server developed in Python. The server is designed to inspect incoming HTTP requests for malicious headers and block those that match a predefined list. The core functionality is implemented using Python's http.server module, extending BaseHTTPRequestHandler to perform header analysis and send a 403 Forbidden response for malicious requests.

### Background Information:
Work with the networks team to implement a firewall rule using the Python scripting language. Python is a common scripting language used across both offensive and defensive information security tasks. In this task, we will simulate the firewall’s scripting language by using an HTTP Server. You can assume this HTTP Server has no computational requirements and has the sole purpose of filtering incoming traffic. In the starter codebase, you will find a test script that you can use to simulate the malicious requests to the server. You can check out the Readme file in the starter codebase for more information on how to get started.

### Task:
Use Python to develop a firewall rule to mitigate the attack. Develop this rule in `firewall_server.py` and only upload this file back here. You may use `test_requests.py` to test your code whilst the firewall HTTP server is running.

### Task 3 Resources:
- [Spring4Shell Proof of Concept Payload](https://github.com/craig/SpringCore0day/blob/main/exp.py)
- [Python HTTPServer documentation](https://docs.python.org/3/library/http.server.html)
- [Firewall Starter Codebase](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T3%20Firewall%20Starter%20Codebase.zip)

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

### Background Information:
The firewall rule worked in stopping the malware attack, 2 hours after the attack began. After an incident has occurred, it’s best practice to document and record what has happened. A common report written after an incident is a postmortem, which covers a timeline of what has occurred, who was involved in responding to the incident, a root cause analysis and any actions which have taken place. The purpose of the postmortem is to provide a ‘paper trail’ of what happened, which may be used in future governance, risk, or compliance audits, but also to educate the team on what went down, especially for those on the team who weren’t involved. In the resources section, you will find some educational content about what is an incident postmortem and why it’s important to create one.

### Task:
For this task, create an incident postmortem of the malware attack, covering the details you have picked up in the previous tasks. Make sure to include when the incident started and the root cause. Remember, the more detail the better.

### Task 4 Resources:
- [What is an incident postmortem](https://www.pagerduty.com/resources/digital-operations/learn/incident-postmortem/)
- [Postmortem Template](https://github.com/s-estrada/TelstraCybersecurityAnalyst/blob/main/T4%20-%20Postmortem%20Template.docx)

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
