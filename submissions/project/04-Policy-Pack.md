# Policy Pack - UKC Ljubljana

This is a minimum viable policy pack for UKC Ljubljana. Because we are doing the analysis on a big organization, the minimum viable policy pack includes 10 policies.

## 1. Access Control Policy

- Hospital enforces role-based access control (RBAC) across all information systems to ensure users only access data required for their job functions.
- The principle of least privilege is applied to all users, including clinical, administrative, and technical staff.
- Multifactor authentication is required for all cloud services, email systems, and privileged accounts.
- Privileged accounts are assigned to individual users and must not be shared.
- Access rights are reviewed on a regular basis, with critical systems reviewed at least every three months.
- Access to systems is revoked immediately when an employee changes roles or leaves the organisation.

## 2. Backup & Recovery Policy

- Hospital performs regular backups of all critical systems, including patient records.
- Backups for critical systems are performed daily to ensure minimal data loss in the event of an incident.
- 3-2-1 backup strategy is implemented to ensure resilience against data loss and ransomware attacks.
- Quarterly tests of backup restoration to ensure recoverability.
- Recovery objectives are defined based on system criticality.

## 3. Incident Response Policy

- All security incidents must be reported immediately to the IT manager and senior management.
- An incident response team is defined, including the IT manager, security officer, and operations lead.
- Incident handling follows the steps: identify, contain, eradicate, recover, and learn.
- Incidents are classified based on severity, depending on their patient care, system availability, and data security.
- Communications are coordinated with legal, compliance, and management before external disclosure.
- Post-incident review and lessons learned are documented and used to improve controls.

## 4. Vendor Security Policy

- All third-party vendors are required to undergo a security check before being granted access to hospital systems.
- Vendor contracts must include explicit cybersecurity and data protection obligations, including GDPR compliance.
- Vendors are granted only the minimum level of access required to perform their services.
- Vendor access is time-limited and subject to monitoring by the hospital IT security team.
- High-risk vendors are reviewed on an annual basis to ensure continued compliance with security requirements.

## 5. Acceptable Use Policy

- Hospital IT systems are used only for authorized professional and clinical purposes.
- Users are prohibited from sharing passwords.
- Users must not copy or transmit sensitive patient data outside approved systems.
- Installation of unauthorized software on hospital devices is not permitted.
- Sensitive patient data must not be stored on local devices without approval.
- Users must immediately report any suspicious emails or potential phishing attempts.

## 6. Network Security Policy

- Hospital network is segmented to separate clinical systems, administrative systems, medical devices, and guest networks.
- Legacy protocols and unnecessary services are disabled to reduce attack surface exposure.
- Network traffic is continuously monitored for anomalies and potential security threats.
- Firewall rules are reviewed regularly to ensure only authorized communication paths are permitted.

## 7. Medical Device Security Policy

- All medical devices are operated within segmented and controlled network environments.
- Devices that cannot be regularly patched are isolated from general IT systems to reduce risk exposure.
- Medical devices used in critical care environments are continuously monitored for availability and integrity.
- Access to medical device management interfaces is restricted to authorised personnel only.

## 8. Cloud and Identity Security Policy

- Multi-factor authentication is required for all access to cloud-based systems.
- User accounts are assigned the minimum level of privileges necessary to perform their duties.
- Administrative cloud activities are logged and monitored for suspicious behavior.
- Cloud access logs are regularly reviewed to detect potential account compromise or misuse.

## 9. Physical Security and Infrastructure Policy

- Access to restricted areas such as server rooms and data centers is controlled using electronic badge systems.
- CCTV systems are deployed across critical infrastructure areas.
- Building management systems are isolated from external networks wherever possible to reduce cyber-physical risk.
- Critical infrastructure systems include manual override capabilities to ensure operational continuity during system failures.
- Emergency systems such as helipad lighting are protected against unauthorized modification or shutdown.

## 10. Security Monitoring and Compliance Policy

- All critical systems are continuously monitored using centralized logging.
- Security alerts are reviewed on a daily basis by designated IT security personnel.
- The hospital maintains compliance with GDPR and other relevant healthcare regulations.
- Regular audits are conducted to ensure adherence to internal policies and external regulations.
