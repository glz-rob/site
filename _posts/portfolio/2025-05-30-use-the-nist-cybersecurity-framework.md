---
layout: post
title:  "Multimedia Company: Use the NIST Cybersecurity Framework to respond to a security incident"
date:   2025-05-30
categories: portfolio security
---

# Scenario

You are a cybersecurity analyst working for a multimedia company that offers web design services, graphic design, and social media marketing solutions to small businesses. Your organization recently experienced a `DDoS attack`, which compromised the internal network for two hours until it was resolved.

During the attack, your organization’s network services suddenly stopped responding due to an incoming `flood of ICMP packets`. Normal internal network traffic could not access any network resources. The incident management team responded by blocking incoming ICMP packets, stopping all non-critical network services offline, and restoring critical network services.

The company’s cybersecurity team then investigated the security event. They found that a malicious actor had sent a flood of ICMP pings into the company’s network through `an unconfigured firewall`. This vulnerability allowed the malicious attacker to overwhelm the company’s network through a distributed denial of service (DDoS) attack.

To address this security event, the network security team implemented:

- A new firewall rule to limit the rate of incoming ICMP packets

- Source IP address verification on the firewall to check for spoofed IP addresses on incoming ICMP packets

- Network monitoring software to detect abnormal traffic patterns

- An IDS/IPS system to filter out some ICMP traffic based on suspicious characteristics

As a cybersecurity analyst, you are tasked with using this security event to create a plan to improve your company’s network security, following the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF). You will use the CSF to help you navigate through the different steps of analyzing this cybersecurity event and integrate your analysis into a general security strategy. We have broken the analysis into different parts in the template below. You can explore them here:

- **Identify** security risks through regular audits of internal networks, systems, devices, and access privileges to identify potential gaps in security.

- **Protect** internal assets through the implementation of policies, procedures, training and tools that help mitigate cybersecurity threats.

- **Detect** potential security incidents and improve monitoring capabilities to increase the speed and efficiency of detections.

- **Respond** to contain, neutralize, and analyze security incidents; implement improvements to the security process.

- **Recover** affected systems to normal operation and restore systems data and/or assets that have been affected by an incident.

# Incident Report Analysis

## Instructions

| Summary   | The company experienced a DDoS attack that rendered our system unsuable for 2 hours until the response team was able to fix it. The network services were flooded with ICMP packets, this overwhelmed tha organization's servers. The cybersecurity team found that the malicious actor managed to do this thanks to an unconfigured firewall. |
| :---      | :---  |
| Identify  | The cybersecurity team audited the organization's network devices affected by the attack to find the vulnerabilities that were abused. The team found out that a miscongfiguration on the network's firewall allowed the threat actor's communication. It appears that the threat actor used this misconfiguration to flood the internal servers with ICMP packets. |
| Protect   | The team has implemented multiple security measures to be able to protect against this kind of threats in the future. The first of them is that a new firewall rule was added to limit the amount of incoming ICMP packets. Source IP address verification was also added to the firewall to prevent traffic with spoofed IP addresses. An IDS/IPS system was also added, this will help filter out ICMP traffic. |
| Detect    | For anomaly detection a network monitoring software was implemented, this will allow the team to detect any abnormal traffic patterns. The IDS/IPS will also alert on any traffic with suspicious characteristics. |
| Respond   | The security operations blocked the incoming traffic ICMP packets, and stopped all non-critical network services. For future security incidents the cybersecurity team will isolate the systems affected to prevent further disruption. They will attempt to restore any critical system affected by the event. |
| Recover   | To restore from DDoS attack, access to network services need to be restored to a normal functioning state, starting with the most critical services first. |

---

| Reflections/Notes:    |
| :---                  |
| The security team don't decide if we are targeted by a DDoS attack or not, but we can always establish the most up-to-date security measures to maintain business continuity, and safeguard our assets. |