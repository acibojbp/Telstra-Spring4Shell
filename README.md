# Telstra Cybersecurity Simluation - Spring4Shell (CVE-2022-22965)

Welcome to my Telstra Cyber Simulation Solutions Repository! Within these digital walls, you'll find a detailed account of my expedition through the Telstra cyber simulation, where I assumed the role of a vigilant security analyst. From the initial alert triage to crafting incident response strategies and developing innovative firewall rules, this repository chronicles my journey in combating cyber threats head-on. Join me as I unravel the intricacies of cybersecurity and shed light on the critical role individuals play in fortifying digital landscapes against ever-evolving adversaries.

### Disclaimer

_Before proceeding with this simulation, it's essential to note that it involves the handling of malware. Please ensure that you conduct these tasks in a controlled and secure environment to prevent any unintended consequences. Always prioritize safety and adhere to cybersecurity best practices while engaging with this simulation._

_All information provided in this repository is sourced directly from the program itself._

## Task 1 - Responding to a malware attack

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



## Task 2 - Analysing the attack

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

