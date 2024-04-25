# Telstra Cybersecurity Simluation - Spring4Shell (CVE-2022-22965)

Welcome to my Telstra Cyber Simulation Solutions Repository! Within these digital walls, you'll find a detailed account of my expedition through the Telstra cyber simulation, where I assumed the role of a vigilant security analyst. From the initial alert triage to crafting incident response strategies and developing innovative firewall rules, this repository chronicles my journey in combating cyber threats head-on. Join me as I unravel the intricacies of cybersecurity and shed light on the critical role individuals play in fortifying digital landscapes against ever-evolving adversaries.

### Disclaimer

_Before proceeding with this simulation, it's essential to note that it involves the handling of malware. Please ensure that you conduct these tasks in a controlled and secure environment to prevent any unintended consequences. Always prioritize safety and adhere to cybersecurity best practices while engaging with this simulation._

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

```
From: Telstra Security Operations
To: NBN Team (nbn@email)
Subject: Urgent: Ongoing NBN Connection Malware Attack - March 20th, 2022, at 3:16:34 UTC

Body:

Hello NBN Team,

We identified a malware attack targeting the NBN Connection infrastructure (nbn.external.network) on March 20th, 2022, at 3:16:34 UTC. This incident has resulted in an ongoing service outage for NBN connections.

Given the critical nature of NBN services, we urge you to initiate an immediate incident response to further mitigate the attack and restore service functionality as quickly as possible. 

For any questions or assistance, please don't hesitate to contact the Telstra Security Operations Center.

Kind regards,
Telstra Security Operations
```
