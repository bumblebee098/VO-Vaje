# Security Improvement Plan

Enrollment Number: 35250009

### 1. Security Maturity Assessment

GreenFields currently operates at a low cybersecurity maturity level.

It currently has no formal security processes, policies, or governance structures it could follow, and security controls are mostly reactive or missing (they are not preventive).

Critical weaknesses identified include:
- poor access control (shared administrator passwords)
- no network segmentation
- absence of monitoring and incident response
- limited backup resilience
- no employee awareness training

The company is exposed to high impact cyber risks, especially ransomware and credential-based attack, based on the recent incidents.

---

### 2. Top 10 Security Risks

1. Ransomware Attack

GreenFields is highly vulnerable to ransomware attack due to:
- lack of network segmentation
- weak backup strategy (backups are stored on the same network and do not follow 3-2-1 rule)
- no monitoring or detection

If a ransomware would be successful in spreading across the system, it could halt production operations, which could lead to financial loss and supply chain disruption.

2. Credential compromise - phishing and password attacks

The company has already experienced a phishing incident, which indicates high exposure.

Risks that could lead to potential credential compromise include:
- no MFA (multi-factor authentication)
- no phishing training for employees
- usage of cloud services, which are accessable from anywhere

Potential further risk with stolen credentials include:
- access to emails and sensitive data
- internal phishing attacks
- escalation of privileges in the network

3. Shared administrator accounts

Multiple users share the same administrator credentials which increases the risk of credential leak and makes privilege escalation for attackers easier. There is also no accountability (no way to track which user performed which actions). If compromised, the attackers could gain full control of systems without detection.

4. Flat network architecture (no segmentation)

All systems (corporate, production, and guest WiFi) are connected to the same network. This means that production systems are directly exposed to threats. It also makes it easier for an attacker to enter through a weak point (like a laptop or WiFi) to move laterally to critical systems.

5. Unsecured backups

Backups are stored on the same network as production systems. There exsists no offline or immutable copies. If ransomware attack is successful, it would encrypt both live data and backups and the company has no ability to recover the data without paying the ransom.

6. Unpatched systems

Company has inconsistent patch management. This means that known vulnerabilities remain exploitable for the attackers. This is one of the most common entry points for cyberattacks.

7. Lack of monitoring, detection, and logging

There is no centralized monitoring or alerts. The company therefore has no visibility into suspicious behavious, which means that attacks could go days or weeks without being noticed.

8. No incident response plan

Company has no defined process for handling of security incidents, which could lead to slow response times and poor communication internally and externally. 

9. Lost or stolen devices

Company has already experienced a loss of a laptop containing internal data. If the device was not encrypted, it could lead to data loss and potential unauthorized access to company systems. Mobile devices also pose a risk.

10. Low employee security awareness

Employees are not trained in cybersecurity safe practices. This increases the risk of phishing attacks, weak password usage, and unsafe handling of sensitive data. With humans being the weakest link in security, this area of risk also affects all other areas.

---

### 3. Priority Security Improvements

1. Implement MFA (Multi-factor authentication)

- apply it to: Microsoft 365, VPN, and admin accounts
- why: MFA adds a second verification factor, which blocks the majority of credential-based attacks. Given that the company already experienced a phishing incident, this is a high impact, low cost improvement.

2. Eliminate shared accounts and enforce identity management

- unique accounts for all users
- RBAC (Role Based Access Control)
- why: improves accountability, where actions can be traced back o individuals. It also follows least privilege access, where users can only access what they need to be operational. It also reduces the attack surface if one account is compromised.

3. Network segmentation

- separate: corporate IT, production systems, and guest WiFi
- why: Flat network allows attackers to move freely once inside. Segmentation acts as a containment mechanism, limiting this.

4. Secure backup strategy (3-2-1 rule)

- have 3 copies of the data, on 2 different media, 1 of which is in another location
- to have offline backups and perform regular restore testing
- why: backups are a defense against a ransomware attack. If the are compromised, recovery becomes impossible without paying ransom. Offline backups ensure that a company can restore operations quickly after the attack.

5. patch management process

- centralize patching on all acounts and perform a monthly patch cycle
- why: most cyberattacks exploit known vulnerabilities with available fixes. Patch management reduces the number of exploitable entrypoints.

6. Endpoint Protection and EDR

- deploy antivirus software and andpoint detection and response on user's workstations and systems
- why: it detects and stops attacks early. EDR can detect threats and isolate infected machines.

7. Security awareness training

- perform annual training for all employees
- perform phishing simulations
- why: reduces human-related risks.

8. Security Monitoring (SIEM)

- have a system that collects logs (Microsoft 365, enpoints, servers)
- it provides alerts for suspicious activity
- why: it enables early detection of attacks and leads to faster response to incidents.

9. Incident response plan

- make a plan and define roles, contacts, and procedures
- conduct exercises
- why: without a plan response is slow and uncoordinated, and mistakes are more likely to happen. A proper plan reduces response time and damage, and helps minimize operational impact.

10. Device security controls

- full disk encryption
- mobile device management
- remote capability to wipe the managed devices
- why: lost or stolen devices can expose sensitive data. Encryption makes sure data remains protected.

---

### 4. Implementation Roadmap

**Phase 1 — Immediate improvements (0-3 months)**

- enable MFA (Microsoft 365, VPN)
- remove shared accounts and make unique accounts
- start making regular backups
- deploy disk encryption on laptops
- start basic security awareness training

**Phase 2 — Medium-term improvements (3-9 months)**

- implement network segmentation
- deploy EDR
- create incident response plan
- establish a patch management process
- introduce centralized logging and/or monitoring

**Phase 3 — Strategic improvements (9-18 months)**

- conduct a formal risk assessment
- implement SIEM or managed SOC service
- perform a penetration test
- make improvements to access control (RBAC)
- perform regular phishing simulatins and audits

---

### 5. Estimated Budget Allocation

| Category | Estimated Cost | Notes |
| --- | --- | --- |
| Security tools (MFA, EDR, MDM) | €30,000        | i.e. Microsoft Defender |
| Monitoring / SIEM / MSSP       | €20,000        | managed security service provider with focus on Microsoft 365 |
| Training & awareness           | €5,000         | Phishing simulations, employee awarness training |
| External consulting            | €15,000        | Risk assessment, segmentation design |
| Backup improvements            | €5,000         | Offline/immutable storage |
| Contingency                    | €5,000         | Unexpected needs and expenses |

---

### 6. Metrics for Measuring Security Improvement

1. Phishing click rate

- target: <5% within 1 year

2. Patch compliance rate

- percentage of systems patched within 14 days
- target: >90%

3. MFA coverage

- percent of users / (divided by) accounts with MFA enabled
- target: 100% for critical systems

4. Backup success and restore rate

- percent of successful backups and test restores
- target: 100% success, quarterly restore tests

5. Mean time to detect

- time to detect incidents
- target: continuous improvemnt