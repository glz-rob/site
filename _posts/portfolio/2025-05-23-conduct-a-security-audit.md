---
layout: post
title:  "Botium Toys: Security Audit"
date:   2025-05-23
categories: portfolio security
---

## Scenario

This scenario is based on a fictional company:

> Botium Toys is a small U.S. business that develops and sells toys. The business has a single physical location, which serves as their main office, a storefront, and warehouse for their products. However, Botium Toy’s online presence has grown, attracting customers in the U.S. and abroad. As a result, their information technology (IT) department is under increasing pressure to support their online market worldwide.

> The manager of the IT department has decided that an internal IT audit needs to be conducted. She's worried about maintaining compliance and business operations as the company grows without a clear plan. She believes an internal audit can help better secure the company’s infrastructure and help them identify and mitigate potential risks, threats, or vulnerabilities to critical assets. The manager is also interested in ensuring that they comply with regulations related to internally processing and accepting online payments and conducting business in the European Union (E.U.).

> The IT manager starts by implementing the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF), establishing an audit scope and goals, listing assets currently managed by the IT department, and completing a risk assessment. The goal of the audit is to provide an overview of the risks and/or fines that the company might experience due to the current state of their security posture.

> Your task is to review the IT manager’s scope, goals, and risk assessment report. Then, perform an internal audit by completing a controls and compliance checklist.

---

## Controls and Compliance Checklist

### Compliance Assessment

Select "yes" or "no" to answer the question: *Does Bitum Toys currently have this control in place?*

#### Controls assessment checklist

| Yes | No  | Control   |
|:---:|:---:|:--------- |
|     |  x  | Least Privilege                                                       |
|     |  x  | Disaster recovery plans                                               |
|     |  x  | Password policies                                                     |
|     |  x  | Separation duties                                                     |
|  x  |     | Firewall                                                              |
|     |  x  | Intrusion detection system (IDS)                                      |
|     |  x  | Backups                                                               |
|  x  |     | Antivirus software                                                    |
|     |  x  | Manual monitoring, maintenance, and intervention for legacy systems   |
|     |  x  | Encryption                                                            |
|     |  x  | Password management system                                            |
|  x  |     | Locks (offices, storefront, warehouse)                                |
|  x  |     | Closed-circuit television (CCTV) suveillance                          |
|  x  |     | Fire detection/prevention (fire alarm, sprinkler system, etc.)        |


### Compliance Assessment

Select "yes" or "no" to answer the question: *Does Botium Toys currently adhere to this compliance best practice?*

#### Compliance checklist

##### Payment Card Industry Data Security Standard (PCI DSS)

| Yes | No  | Best practice   |
|:---:|:---:|:--------- |
|     |  x  | Only authorized users have access to customers' credit card information. |
|     |  x  | Credit card information is stored, accepted, processed, and transmitted internally, in a secure environment. |
|     |  x  | Implement data encryption procedures to better secure credit card transaction touchpoints and data. |
|     |  x  | Adopt secure password management policies. |

##### General Data Protection Regulation (GDPR)

| Yes | No  | Best practice   |
|:---:|:---:|:--------- |
|     |  x  | E.U. customers' data is kept private/secured. |
|  x  |     | There is a plan in place to notify E.U. customers within 72 hours if their data is compromised/there is a breach. |
|  x  |     | Ensure data is properly classified and inventoried. |
|  x  |     | Enforce privacy policies, procedures, and processess to properly document and maintain data. |

##### System and Organizations Controls (SOC type 1, SOC type 2)

| Yes | No  | Best practice   |
|:---:|:---:|:--------- |
|     |  x  | User access policies are established. |
|     |  x  | Sensitive data (PII/SPII) is confidential/private. |
|  x  |     | Data integrity ensures the data is consistent, complete, accurate, and has been validated. |
|     |  x  | Data is available to individuals authorized to access it. |

### Recommendations (optional)

- A good place to start would be with establishing user access policies.

- The following step would be to create backups, and implement data encryption.

- Once user access policies are implemented and centrilized with a service like Windows Active Directory or something similar, password policies and role privileges can be easily asigned.

- An Intrusion Detection System should be implemented along the Active Directory.

- Creating a monitoring schedule for legacy systems must be in mind, another solution would be to migrate to a newer technology.