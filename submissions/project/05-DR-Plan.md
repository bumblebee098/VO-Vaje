# Disaster Recovery Plan (DRP)

## 1. Organization Information

- Organization Name: University Medical Centre Ljubljana (UKC Ljubljana)
- Address: Zaloška cesta 2, 1000 Ljubljana, Slovenia
- IT Department Contact: IT Operations Department / CISO Office
- DR Plan Owner: IT Director
- Date Created: May 2026
- Last Updated: May 2026

---

# 2. Purpose

This Disaster Recovery Plan defines the procedures and responsibilities required to restore critical IT systems and clinical services following a disruption such as cyberattack, system failure, data corruption, or other outages.

The goal is to ensure continuity of patient care by minimizing downtime, protecting clinical data integrity, and restoring essential hospital services as quickly as possible.

---

# 3. Scope

This plan applies to all critical and high-priority hospital systems, including clinical, administrative, and infrastructure systems.

| System                               | Description                             | Criticality |
| ------------------------------------ | --------------------------------------- | ----------- |
| A1 – Electronic Health Records (EHR) | Central patient record system           | Critical    |
| A3–A5 – Clinical Systems             | Radiology, lab, pharmacy systems        | Critical    |
| A7 – Appointment System              | Patient scheduling system               | High        |
| A10 – Insurance Claims System        | External billing system                 | Medium      |
| A12 – Hospital Information System    | Integrated hospital operations platform | Critical    |
| A13 – Active Directory               | Identity and access management system   | Critical    |
| A14 – Email System                   | Communication system                    | High        |
| A17 – Backup and Recovery System     | Data restoration infrastructure         | Critical    |

---

# 4. Disaster Recovery Objectives

Because UKC Ljubljana operates as critical healthcare infrastructure, recovery objectives are significantly shorter compared to non-critical organizations to ensure continuity of patient care and clinical operations.

| System                   | Recovery Time Objective (RTO) | Recovery Point Objective (RPO) |
| ------------------------ | ----------------------------- | ------------------------------ |
| A1 – EHR System          | 1-2 hours                       | 15-30 minutes                         |
| A3–A5 – Clinical Systems | 2-4 hours                       | 1 hour                        |
| A7 – Appointment System  | 4-8 hours                       | 2-4 hours                        |
| A12 – HIS                | 2-4 hours                       | 1 hour                         |
| A13 – Active Directory   | 1 hour                       | 30 minutes                     |
| A14 – Email System       | 8-24 hours                       | 4-24 hour                         |
| A17 – Backup System      | 24-72 hours                      | 24-48 hours                       |

Brief explanation:
- Email system is important, but not clinical-critical.
- Backup system is a recovery system and is not real-time dependent.

---

# 5. Disaster Recovery Team

| Role                 | Name / Title      | Responsibility                     | Contact |
| -------------------- | ----------------- | ---------------------------------- | ------- |
| DR Manager           | IT Director       | Coordinates recovery and decisions |         |
| System Administrator | Systems Admin     | Restoration of servers and applications           |         |
| Network Engineer     | Network Admin     | Restoration of network connectivity and segmentation     |         |
| Security Officer     |CISO               | Manages incident response          |         |
| Clinical IT Liaison   | IT Manager       | Coordination with hospital departments

---

# 6. Backup Strategy

Critical hospital systems are protected through a layered backup strategy, which is designed to ensure resillience agains ransomware and system failure.

| System              | Backup Type        | Frequency      | Location                     |
| ------------------- | ------------------ | -------------- | ---------------------------- |
| A1 – EHR            | Full + Incremental | Daily / Hourly | Off-site + cloud             |
| A3–A5               | Incremental        | Daily          | Backup server                |
| A12 – HIS           | Full + Incremental | Daily          | Off-site backup centre       |
| A13 – AD            | Full               | Daily          | Offline + secure backup      |
| A17 – Backup System | Replicated         | Continuous     | Off-site + immutable storage |

---

# 7. Disaster Scenarios

Within this plan we consider the following scenarios:

- Ransomware attacks affecting clinical and administrative systems.
- Hardware or server failure within the data cente (A23).
- Loos or corruption of patient data (A1, A2).
- Network outages affecting hospital-wide systems (A15).
- Power outages impacting critical infrastructure (A24).
- Cloud service outages affecting SaaS systems (A7, A10, A14).
- Physical damage to IT infrastructure due to natural disasters.

---

# 8. Recovery Procedures


## 8.1 Ransomware Attack

Steps:

1. Immediately isolate infected systems from the hospital network.
2. Identify affected systems through security monitoring tools.
3. Verify backup integrity before restoration.
4. Restore systems in order of clinical priority.
5. Reset compromised credentials and apply containment controls.
6. Conduct a forensic investigation and document the incident.

---

## 8.2 Server or System Failure

Steps:

1. Identify the failed system and isolate it if necessary.
2. Notify the DR Manager and the recovery team.
3. Activate backup infrastructure and restore the latest clean backup.
4. Verify system integrity and data consistency.
5. Reconnect users and confirm service restoration.

---

## 8.3 Data Loss or Corruption

Steps:

1. Identify the extent of data loss.
2. Retrieve the most recent valid backup.
3. Validate and then restore the data to a clean environment.
4. Clinical departments are notified once systems are confirmed to be stable.
4. Resume operations and update the restoration documentation.

---

## 8.4 Network or Infrastructure Outage

Steps:

1. Isolate netowkr failure and identify root cause.
2. Activate backup network routes or backup systems.
3. Prioritize critical systems for restoration.
4. Restore to full connectivity.

---

# 9. Communication Plan

| Situation              | Responsible         | Communication Method             |
| ---------------------- | ------------------- | -------------------------------- |
| System outage          | IT Operations Team  | Internal alert system / email    |
| Critical incident      | DR Manager + CISO   | Emergency call + incident bridge |
| Clinical disruption    | IT + Clinical Lead  | Direct hospital escalation       |
| External communication | Hospital Management | Official hospital statement      |


---

# 10. Testing and Maintenance

The Disaster Recovery Plan must be tested regularly to ensure effectiveness and readiness.

| Test Type                    | Frequency |
| ---------------------------- | --------- |
| Backup restore test          | Quarterly |
| Disaster simulation          | Annually  |
| Security incident simulation | Annually  |

All test results are documented and used to imprve recovery procedures.

---

# 11. Plan Review

This Disaster Recovery Plan is reviewed:

- After any major infrastructure or system changes.
- Following any major cybersecurity incident.
- At minimum, once per year.

The IT Director is responsible for ensuring updates are completed and approved.

---

# 12. Approval

| Name                | Role              | Signature | Date |
| ------------------- | ----------------- | --------- | ---- |
| IT Director         | DR Plan Owner     |           |      |
| CISO                | Security Approval |           |      |
| Hospital Management | Final Approval    |           |      |
