# Cybersecurity Risk Assessment Project - UKC Ljubljana

Enrollment Number: 35250009

## 1. Organisation Overview

University Medical Centre Ljubljana (UKC Ljubljana) is the largest public healthcare institution in Slovenia.

It provides:

- emergency and acute care services
- specialist outpatient and inpatient treatment
- advanced diagnostic services (radiology, laboratory, imaging)
- surgical and intensive care services
- national-level referral healthcare for complex cases

**Employees:** ~8,000+ (clinical, administrative, and support staff)
IT staff: Central IT department (IT operations, cybersecurity team, infrastructure engineers).

**Operating model:** Public healthcare institution funded by national healthcare system.

UKC Ljubljana is highly dependent on digital systems to support patient care, clinical decision-making, and hospital operations.

## 2. IT Environment

### Infrastructure

Hybrid environment (on-premise + cloud-based services)

**On-premise systems:**

- Hospital data centre hosting critical clinical systems
- Active Directory for identity and access management
- Hospital Information System (HIS)
- Clinical systems (radiology, laboratory, pharmacy, scheduling)
- Backup and recovery infrastructure (off-site replication included)

**Cloud systems:**

- Email systems (SaaS-based),
- Insurance claims processing platform,
- Appointment booking system,
- External healthcare integration services.

### Endpoints
- Clinical workstation computers across departments
- Administrative office PCs and laptops
- Medical devices with embedded computing capabilities
- Mobile devices used by healthcare staff (tablets, handheld devices)

### Network
- Segmented hospital-wide network (clinical, administrative, guest, and medical device zones)
- Dedicated network segments for critical care systems (ICU, radiology, lab)
- Centralised firewall, IDS, and IPS systems
- Guest Wi-Fi network

## 3. Data Types

- Patient electronic health records (special category health data under GDPR)
- Medical imaging data (MRI, CT, X-ray scans)
- Laboratory test results and diagnostics
- Prescription and pharmacy records
- Employee HR and payroll data
- Financial and billing information
- Insurance claims and reimbursement data
- System logs and security audit data

## 4. Business Processes

- Patient registration and admission
- Emergency care and ICU treatment
- Appointment scheduling and outpatient management
- Radiology and diagnostic imaging
- Laboratory testing and reporting
- Pharmacy and medication dispensing
- Surgical scheduling and theatre management
- Billing, insurance claims, and financial processing
- Internal communication and clinical coordination

## 5. Known Issues (Assumed / Industry-Realistic Risks)

- Increased exposure to phishing attacks targeting hospital staff
- High dependency on legacy clinical systems in certain departments
- Complex hybrid IT environment increasing attack surface
- Critical reliance on availability of electronic health records systems
- Limited tolerance for downtime in emergency and ICU services
- Integration between multiple clinical systems introduces interoperability risks
- High-value personal health data makes the organisation a target for ransomware attacks

## 6. Regulatory Context

- General Data Protection Regulation (GDPR) – processing of special category health data
- Slovenian healthcare legislation and national data protection requirements
- EU cybersecurity expectations for critical infrastructure organisations
- Clinical safety and patient care continuity obligations
- Internal hospital governance and IT security policies