# Disaster Recovery Plan (DRP) Template

## 1. Organization Information

- Organization Name: BlueRiver Health Ltd.
- Address: Two-city private healthcare provider
- IT Department Contact: IT Manager
- DR Plan Owner: IT Manager
- Date Created: April 2026
- Last Updated: April 2026

---

# 2. Purpose

This Disaster Recovery Plan describes the procedures and responsibilities required to recover BlueRiver Health IT systems and data after disruption such as ransomware, hardware failure, or service outage.

The goal is to minimize patient care disruption, protect sensitive health data, and restore business operations quickly.

---

# 3. Scope

This plan applies to the following systems:

| System                    | Description                                   | Criticality |
| ------------------------- | --------------------------------------------- | ----------- |
| Web server                | Public website                                | High        |
| Microsoft 365 Email       | Email and collaboration                       | High        |
| ERP system                | Business management                           | Critical    |
| Patient Database          | Clinical records and patient data             | Critical    |
| Telemedicine Platform     | Remote consultation service                   | Critical    |
| Active Directory          | Identity and authentication infrastructure    | Critical    |
| Local NAS Backup          | Backup storage for systems                    | Critical    |
| Shared File Server        | Administrative and clinical document storage  | High        |

---

# 4. Disaster Recovery Objectives

| System                    | RTO                         | RPO                         |
| ------------------------- | --------------------------- | --------------------------- |
| Patient Database          | 4 hours                     | 1 hour                      |
| Telemedicine Platform     | 4 hours                     | 1 hour                      |
| Active Directory          | 6 hours                     | 2 hours                     |
| Microsoft 365 Email       | 6 hours                     | 2 hours                     |
| Shared File Server        | 8 hours                     | 2 hours                     |
| Local NAS Backup          | 6 hours                     | 2 hours                     |

---

# 5. Disaster Recovery Team

| Role                 | Name / Title      | Responsibility                     | Contact |
| -------------------- | ----------------- | ---------------------------------- | ------- |
| DR Manager           | IT Manager        | Coordinates recovery and decisions |         |
| System Administrator | Systems Admin     | Restores servers and VMs           |         |
| Network Engineer     | Network Admin     | Restores network connectivity      |         |
| Security Officer     | IT Manager        | Manages incident response          |         |

---

# 6. Backup Strategy

| System                  | Backup Type     | Frequency     | Location                  |
| ----------------------- | --------------- | ------------- | ------------------------- |
| Patient Database        | Full / incremental | Daily       | Local NAS + offsite      |
| Shared File Server      | Incremental     | Daily         | Local NAS + offsite       |
| Microsoft 365 Email     | Cloud backup    | Daily         | Vendor cloud storage      |
| Active Directory        | System state    | Daily         | Local NAS + offsite       |


Backup locations:

- Cloud backup (AWS / Azure)
- Encrypted offsite backup storage
- Offline backup (air-gapped storage)
- Local NAS backup device

---

# 7. Disaster Scenarios

Possible disasters include:

- Cyber attack (ransomware)
- Hardware or server failure
- Data corruption or deletion
- Network outage
- Power outage
- Natural disaster (fire, flood)

---

# 8. Recovery Procedures

## 8.1 Server Failure

Steps:

1. Identify the failed server or service.
2. Notify the DR Manager and the recovery team.
3. Activate backup infrastructure and restore the latest clean backup.
4. Verify system integrity and data consistency.
5. Reconnect users and confirm service restoration.

---

## 8.2 Ransomware Attack

Steps:

1. Isolate infected systems and affected network segments.
2. Identify impacted systems and data stores.
3. Confirm backup integrity and restore from clean backup.
4. Reset compromised credentials and apply containment controls.
5. Conduct forensic analysis and document the incident.

---

## 8.3 Data Loss

Steps:

1. Identify the scope and cause of the data loss.
2. Retrieve the most recent valid backup.
3. Restore the data to a clean environment.
4. Verify data integrity and completeness.
5. Resume operations and update the restoration documentation.

---

# 9. Communication Plan

| Situation            | Responsible       | Communication Channel              |
| -------------------- | ----------------- | ---------------------------------- |
| System outage        | IT Manager        | Email / Phone                      |
| Major incident       | DR Manager        | Phone / Emergency meeting          |
| Regulatory notification | Security Officer | Email / Official letter            |
| Public communication | Management        | Press statement / Media response   |

---

# 10. Testing and Maintenance

The Disaster Recovery Plan must be tested regularly.

| Test Type                    | Frequency |
| ---------------------------- | --------- |
| Backup restore test          | Quarterly |
| Disaster simulation          | Annually  |
| Security incident simulation | Annually  |

---

# 11. Plan Review

This plan should be reviewed:

- After major system changes
- After security incidents
- At least once per year

Responsible person: IT Manager

---

# 12. Approval

| Name | Role | Signature | Date |
| ---- | ---- | --------- | ---- |
|      |      |           |      |
