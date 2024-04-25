# Telstra Cybersecurity Simluation - Spring4Shell (CVE-2022-22965)

Welcome to my Telstra Cyber Simulation Solutions Repository! Within these digital walls, you'll find a detailed account of my expedition through the Telstra cyber simulation, where I assumed the role of a vigilant security analyst. From the initial alert triage to crafting incident response strategies and developing innovative firewall rules, this repository chronicles my journey in combating cyber threats head-on. Join me as I unravel the intricacies of cybersecurity and shed light on the critical role individuals play in fortifying digital landscapes against ever-evolving adversaries.

### Disclaimer

_Before proceeding with this simulation, it's essential to note that it involves the handling of malware. Please ensure that you conduct these tasks in a controlled and secure environment to prevent any unintended consequences. Always prioritize safety and adhere to cybersecurity best practices while engaging with this simulation._

_All information provided in this repository is sourced directly from the program itself._

## Contents

- [Task 1: Responding to a malware attack](#task-1-responding-to-a-malware-attack)
- [Task 2: Analysing the attack](#task-2-analysing-the-attack)
- [Task 3: Mitigate the malware attack](#task-3-mitigate-the-malware-attack)
- [Task 4: Incident Postmortem](#task-4-incident-postmortem)

## Task 1: Responding to a malware attack

An alert has come into the Security Operation Centre (SOC). Triage the alert and respond to the malware attack by contacting the appropriate team.

### Here is the background information on your task

You are an information security analyst in the Security Operations Centre. A common task and responsibility of information security analysts in the SOC is to respond to triage incoming threats and respond appropriately, by notifying the correct team depending on the severity of the threat. It’s important to be able to communicate the severity of the incident to the right person so that the organisation can come together in times of attack.

The firewall logs & list of infrastructure has been provided, which shows critical services that run the Spring Framework and need to be online / uninterrupted. A list of teams has also been provided, which depending on the severity of the threat, must be contacted.

It’s important to note that the service is down and functionality is impaired due to the malware attack.

### Here is your task

Your task is to triage the current malware threat and figure out which infrastructure is affected.

First, find out which key infrastructure is currently under attack. Note the priority of the affected infrastructure to the company - this will determine who is the respective team to notify.

After, draft an email to the respective team alerting them of the current attack so that they can begin an incident response. Make sure to include the timestamp of when the incident occurred. Make it concise and contextual.

The purpose of this email is to ensure the respective team is aware of the ongoing incident and to be prepared for mitigation advice.

### Resources to help you with the task

[Spring Releases Security Updates Addressing "Spring4Shell" and Spring Cloud Function Vulnerabilities | CISA](https://www.cisa.gov/news-events/alerts/2022/04/01/spring-releases-security-updates-addressing-spring4shell-and-spring)  
[CVE-2022-22965: Spring Framework RCE via Data Binding on JDK 9+](https://spring.io/security/cve-2022-22965)

**Firewall Infrastructure List:**

| **Infrastructure Software** | **Infrastructure Name** | **Network Hostname**         | **Description**                                                            | **Infrastructure Team** | **Team Lead Email** | **Priority**  |
| --------------------------- | ----------------------- | ---------------------------- | -------------------------------------------------------------------------- | ----------------------- | ------------------- | ------------- |
| Spring Framework 5.3.0      | Mobile Tower Connection | mobiletower.internal.network | Provides a route between mobile towers across the country for cell service | Mobile Team             | mobileteam@email    | P2 - High     |
| Spring Framework 5.3.0      | NBN Connection          | nbn.external.network         | Provides high-speed nbn connection service                                 | nbn Team                | nbn@email           | P1 - Critical |
| Spring Framework 5.3.0      | Home & Business Lines   | homebiz.internal.network     | Provides home & business line products such as VoIP                        | Networks Team           | networks@email      | P2 - High     |
| Spring Framework 5.3.0      | ADSL Connect            | adsl.internal.network        | Provides ADSL product to customers                                         | Networks Team           | networks@email      | P2 - High     |

### Solution

![T1 - Model Answer](https://github.com/acibojbp/Telstra-Spring4Shell/assets/164168280/3ce74596-8242-45e5-911a-36cc72a5853d)  
T1 - Model Answer

[My Answer]

## Task 2: Analysing the attack

Analyse the data of the malware attack to identify how the malware spreads. Find patterns used by the attacker so that we can prepare a firewall rule to stop the spread of the virus.

### Here is the background information on your task

Now that you have notified the infrastructure owner of the current attack, analyse the firewall logs to find the pattern in the attacker’s network requests. You won’t be able to simply block IP addresses, because of the distributed nature of the attack, but maybe there is another characteristic of the request that is easy to block.

An important responsibility of an information security analyst is the ability to work across disciplines with multiple teams, both technical and non-technical.

In the resources section, we have attached a proof of concept payload that may be of interest in understanding how the attacker scripted this attack.

### Here is your task

First, analyse the firewall logs in the resources section.

Next, identify what characteristics of the Spring4Shell vulnerability have been used.

Finally, draft an email to the networks team with your findings. Make sure to be concise, so that they can develop the firewall rule to mitigate the attack. You can assume the recipient is technical and has dealt with these types of requests before.

### Resouces

[Spring4Shell Proof of Concept Payload](https://github.com/craig/SpringCore0day/blob/main/exp.py)

### Solution

![T2 - Model Answer](https://github.com/acibojbp/Telstra-Spring4Shell/assets/164168280/f16b6423-726e-4ed0-aa14-5a5e868b84c1)  
T2 - Model Answer

[My Answer]


## Task 3: Mitigate the malware attack

Using the patterns you’ve identified, use Python to write a firewall rule to technically mitigate the malware from spreading.

### Here is the background information on your task

Work with the networks team to implement a firewall rule using the Python scripting language. Python is a common scripting language used across both offensive and defensive information security tasks.

In this task, we will simulate the firewall’s scripting language by using an HTTP Server. You can assume this HTTP Server has no computational requirements and has the sole purpose of filtering incoming traffic.

In the starter codebase, you will find a test script that you can use to simulate the malicious requests to the server.

You can check out the Readme file in the starter codebase for more information on how to get started.

### Here is your task

Use Python to develop a firewall rule to mitigate the attack. Develop this rule in `firewall_server.py` and only upload this file back here.

You may use `test_requests.py` to test your code whilst the firewall HTTP server is running.

### Resources

[http.server — HTTP servers — Python 3.12.3 documentation](https://docs.python.org/3/library/http.server.html)

### Solution

Running the base `firewall_server.py` script and executing the `test_requests.py` script to observe the firewall's behavior.

![VirtualBox_Windows 10_24_04_2024_19_58_09](https://github.com/acibojbp/Telstra-Spring4Shell/assets/164168280/8df78928-0200-404b-a695-d79b86206a39)

Running the modified `firewall_server.py` script to block any detection of the `Spring4Shell` and using `test_requests.py` to validate the firewall rule.

![VirtualBox_Windows 10_24_04_2024_19_58_56](https://github.com/acibojbp/Telstra-Spring4Shell/assets/164168280/6bfd7b06-5d96-41c3-b113-83bf1854d340)

[Answer Script](./Solutions/firewall_server_T3.py)  
[My Script](./Solutions/firewall_server.py)

## Task 4: Incident Postmortem

### Here is the background information on your task

The firewall rule worked in stopping the malware attack, 2 hours after the attack began.

After an incident has occurred, it’s best practice to document and record what has happened. A common report written after an incident is a postmortem, which covers a timeline of what has occurred, who was involved in responding to the incident, a root cause analysis and any actions which have taken place.

The purpose of the postmortem is to provide a ‘paper trail’ of what happened, which may be used in future governance, risk, or compliance audits, but also to educate the team on what went down, especially for those on the team who weren’t involved.

In the resources section, you will find some educational content about what is an incident postmortem and why it’s important to create one.

### Here is your task

For this task, create an incident postmortem of the malware attack, covering the details you have picked up in the previous tasks.

Make sure to include when the incident started and the root cause. Remember, the more detail the better.

### Resources

[What is an Incident Postmortem? | Articles | PagerDuty](https://www.pagerduty.com/resources/learn/incident-postmortem/)

### Solution

[T4 - Model Answer](./Solutions/T4%20-%20Model%20Answer.pdf)  
[My Answer]
