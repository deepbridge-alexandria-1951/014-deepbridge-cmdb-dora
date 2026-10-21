# DORA and CMDB: Digital Operational Resilience Obligations and Governance Framework

## The Critical Starting Point: DORA Is NOT Just a Technical Resilience Standard

**Before diving into technical requirements, understand this: DORA (Digital Operational Resilience Act) is fundamentally a business and legal framework that imposes mandatory operational resilience governance on financial institutions—not merely a set of technical controls or a disaster recovery checklist.** Many financial institutions treat operational resilience as an IT backup and recovery problem: "Ensure redundancy, maintain backups, and we're compliant." This is a critical misconception that carries severe regulatory and financial consequences.

DORA reshapes how financial institutions manage operational risk by requiring **systematic risk assessment, real-time incident reporting, supply chain security oversight, and executive accountability** for technology-driven failures. For a financial institution deploying a **CMDB (Configuration Management Database)** as critical infrastructure, DORA means you must ensure the CMDB contributes to your institution's operational resilience, and that you can detect, respond to, and report technology-related incidents within **hours**—not days.

The burden falls on the **financial entity** (your institution). DORA applies to all **credit institutions, investment firms, payment institutions, and other regulated financial entities** across the EU. Non-compliance carries **severe penalties, regulatory sanctions, and potential operational restrictions imposed by authorities.** More importantly, failure to manage operational resilience can lead to systemic financial failures affecting customers and markets.

---

## Overview of DORA

**DORA** is the **Digital Operational Resilience Act**, which entered into force in **December 2022** and became applicable on **January 17, 2025**. DORA is the EU's primary regulatory framework for operational resilience in financial services, establishing mandatory requirements for credit institutions, investment firms, payment institutions, and certain other financial entities to maintain resilience against technology-related disruptions.

### What Makes DORA Different from Existing Frameworks?

DORA introduced a paradigm shift in how financial regulators approach operational risk:

| Aspect | Pre-DORA | DORA |
|--------|----------|------|
| **Scope** | Technology risk was part of broader operational risk management | Explicit, detailed framework focused exclusively on digital/technology operational resilience |
| **Incident Reporting** | Serious incidents reported quarterly or annually | **Mandatory reporting of all incidents within 24 hours**; detailed reporting within 10-15 days |
| **Cyber Incident Distinction** | All incidents treated equally | Cyber incidents require **immediate notification to authorities** if significant impact |
| **ICT Risk Tolerance** | Institutions self-determined risk appetite | Regulators define **maximum tolerable downtime** (up to 4 hours for critical functions) |
| **Testing Obligations** | Limited testing requirements | **Mandatory advanced threat-led penetration testing (TLPT)** annually |
| **Supply Chain Oversight** | Limited vendor management | Explicit, detailed supply chain security and incident reporting by critical third parties |
| **Governance** | Risk management delegation to IT | **Board-level oversight** of operational resilience; mandatory board reporting |
| **Penalties** | Up to €1 million per violation (varies by member state) | Up to **€15 million or 2% of turnover** (credit institutions); **€10 million or 2% of turnover** (other entities) |
| **Enforcement** | Reactive regulatory approach | **Proactive regulatory scrutiny**; regulators inspect and audit operational resilience controls |

**The shift is clear: DORA moves operational resilience from an IT function to a board-level strategic priority.**

---

## Scope and Applicability: Who Must Comply?

DORA applies to the following financial institutions:

### Directly Regulated Entities

| Entity Type | Definition | Examples | CMDB Relevance |
|-------------|-----------|----------|----------------|
| **Credit Institutions** | Banks; entities authorized to take deposits and provide credit | All banks, credit unions, mortgage lenders | If CMDB is critical to banking operations |
| **Investment Firms** | Firms providing investment services | Brokerages, asset managers, investment advisors | If CMDB is critical to investment operations |
| **Payment Institutions** | Entities providing payment services | Payment processors, money transfer providers, e-money issuers | If CMDB is critical to payment processing |
| **Insurance Undertakings** | Entities providing insurance | Insurance companies, pension funds | If CMDB is critical to insurance operations |
| **Central Counterparties (CCPs)** | Entities clearing derivatives and securities | Clearinghouses | If CMDB is critical to clearing operations |
| **Trade Repositories** | Entities reporting derivatives transactions | Trade data repositories | If CMDB is critical to reporting operations |
| **Certain Investment Firms (Threshold)** | Firms with >€30 billion in assets or €1 billion annual turnover | Large investment firms | If CMDB is critical to operations |

### Indirect Applicability: Critical Third-Party Providers

Even if your organization is not directly regulated, DORA may apply if you are a:

- **Critical third-party service provider**: Vendor providing essential services to regulated financial institutions (e.g., cloud provider, software vendor, outsourced service provider)
- **Significant third-party service provider**: Vendor providing services that, if disrupted, would have a significant impact on a financial institution's operations

**Critical for CMDB: If you provide CMDB software or hosting services to regulated financial institutions, DORA compliance may be required of you (third-party obligations).**

---

## Core Obligations Under DORA

If DORA applies to your institution, you must satisfy the following mandatory obligations:

### 1. ICT Risk Management Framework (Mandatory)

DORA requires a **comprehensive, integrated ICT risk management framework** covering all technology systems, including CMDB:

#### Establish an ICT Risk Management System
- Identify all ICT systems critical to the provision of financial services
- **Specifically identify the CMDB if it is critical to your operations**
- Assess ICT risks (availability, integrity, confidentiality, authentication, authorization)
- Identify threats (cyber attacks, hardware failures, human error, third-party failures)
- Assess vulnerabilities in systems, processes, and personnel
- Evaluate likelihood and impact of ICT incidents

#### Define Risk Appetite and Risk Tolerance
- Define your institution's **maximum tolerable ICT downtime (MTID)** for critical functions
  - DORA limits MTID: typically **up to 4 hours** for critical financial functions (depending on function criticality)
  - Cannot exceed **24 hours** for any function
- Define acceptable levels for data loss, corruption, or unavailability
- Define acceptable levels of system performance degradation
- **Document and communicate risk appetite to the board**

#### Implement Proportionate ICT Security and Resilience Controls
- Based on risk assessment, implement technical and organizational measures
- Measures must achieve the defined risk appetite (keep incident probability and impact within acceptable levels)
- Examples: encryption, access control, network segmentation, redundancy, backup, disaster recovery, monitoring

#### Monitor and Adjust Controls
- Continuously monitor ICT risks and effectiveness of controls
- Update risk assessment and controls based on changes in threat landscape
- Conduct regular reviews (at least annually) of the ICT risk management framework
- Document monitoring activities and adjustments

#### CMDB-Specific ICT Risk Management
- Classify the CMDB as a critical system if it stores configurations essential to service delivery
- Assess CMDB risks:
  - **Availability**: Can CMDB be recovered within MTID if disrupted?
  - **Integrity**: Can CMDB data be corrupted or tampered with? How would you detect it?
  - **Confidentiality**: Is sensitive configuration data in CMDB adequately protected?
  - **Completeness**: Are all critical systems documented in CMDB? What happens if CMDB data is incomplete?
- Implement controls appropriate to CMDB criticality (likely requires high-level protection)

### 2. Incident Management and Reporting (Mandatory - Major Requirement)

DORA imposes **strict, rapid incident reporting obligations** that represent a significant operational change:

#### Incident Detection and Classification
- Establish procedures to detect all ICT incidents (not just cyber attacks)
- Classify incidents by severity and type:
  - **Cyber incidents**: Security-related incidents (malware, unauthorized access, data breach, etc.)
  - **Non-cyber ICT incidents**: Availability issues, data corruption, system failures, etc.
- Maintain detailed incident logs with timeline, systems affected, and impact

#### Reporting Timeline - CRITICAL
| Incident Type | Reporting Requirement | Timeline |
|---|---|---|
| **Significant cyber incidents** | Notify competent authority (regulator) immediately | **Within 24 hours** of detection |
| **All ICT incidents with significant impact** | Notify competent authority | **Within 24 hours** of detection |
| **Detailed incident report** | Provide comprehensive information to regulator | **Within 10-15 days** (depending on complexity) |
| **Final incident report** | Full root cause analysis, impact, remediation | **As soon as possible**, typically within 30 days |

#### What Qualifies as "Significant Impact"?

An ICT incident has significant impact if it meets any of these criteria:

| Criterion | Example |
|-----------|---------|
| **Unavailability of critical functions** | CMDB is unavailable for >4 hours (or your defined MTID), disrupting service delivery |
| **Data loss or corruption** | Critical CMDB data is corrupted or lost; integrity cannot be assured |
| **Unauthorized access or disclosure** | Sensitive configuration data in CMDB is exfiltrated or exposed to unauthorized parties |
| **Malware infection** | CMDB infrastructure is compromised by ransomware, backdoor, or other malware |
| **Reputational impact** | The incident could harm your reputation or cause customer loss |
| **Financial impact** | The incident causes direct financial losses exceeding a threshold (e.g., >€100,000) |
| **Regulatory breach** | The incident violates regulatory requirements (e.g., data breach under GDPR) |
| **Systemic impact** | The incident could affect financial stability or other institutions |

**Important: Even if an incident is internal and quickly resolved, if it meets any of these criteria, it must be reported within 24 hours.**

#### Incident Report Content (Required Information)
| Information | Description |
|-------------|-------------|
| **Time of detection** | When was the incident first discovered? |
| **Time of occurrence** | When did the incident actually happen? |
| **System(s) affected** | Which ICT systems or services were impacted? (e.g., CMDB, trading systems, payment processing) |
| **Functions affected** | Which critical functions were disrupted? |
| **Duration of impact** | How long was the system unavailable or degraded? |
| **Type of incident** | Cyber attack, system failure, third-party failure, human error, etc. |
| **Attack vector** | How did the attacker gain access? (if cyber incident) |
| **Data involved** | What data was accessed, modified, exfiltrated, or deleted? |
| **Financial impact** | Quantified impact: costs, losses, customer complaints |
| **Remediation measures taken** | What was done to resolve the incident? |
| **Root cause** | What caused the incident? |
| **Preventive measures** | What will be done to prevent recurrence? |
| **External parties involved** | Third-party vendors, law enforcement, incident responders |

#### Notification to Affected Parties
- If personal data was affected, notify affected individuals (GDPR obligation applies in parallel)
- Notify affected customers if services they depend on were disrupted
- Communicate with financial regulators as required
- Maintain transparency with public and stakeholders about significant incidents

### 3. ICT Incident Reporting for Financial Institutions (Mandatory)

DORA requires specific incident reporting to financial regulators:

#### Establish Incident Reporting Processes
- Designate a **point of contact** for incident reporting to regulators (often the CISO or equivalent)
- Establish communication channels with financial authority (central bank, banking supervisor, etc.)
- Ensure 24/7 availability for incident notification (incidents can occur anytime)
- Maintain incident tracking and status updates to regulators

#### Cyber Incidents Requiring Immediate Reporting
- Any cyber incident meeting the "significant impact" threshold must be reported within 24 hours
- Examples:
  - Ransomware affecting CMDB or critical systems
  - Data breach exposing customer or operational data
  - DDoS attack disrupting services
  - Unauthorized access to critical systems

#### Non-Cyber ICT Incidents Requiring Reporting
- System outages lasting >30 minutes for critical functions
- Data corruption or loss affecting critical operations
- Third-party vendor failures disrupting services
- Hardware failures causing availability issues

### 4. Impact Tolerance and Recovery Objectives (Mandatory)

DORA requires institutions to define and maintain strict operational recovery targets:

#### Maximum Tolerable Downtime (MTID)
- Define the **maximum duration** a critical function can be unavailable before unacceptable harm occurs
- MTID is typically **4 hours for critical functions** (e.g., payment processing, settlement)
- Longer for less-critical functions (up to 24 hours maximum)
- **CMDB MTID**: If CMDB is critical to service delivery, define MTID (likely 4 hours or less)

#### Recovery Time Objective (RTO)
- Define the **target time to recover** critical functions after an incident
- RTO must be significantly less than MTID (typically 1-2 hours for critical functions)
- **CMDB RTO**: Ensure CMDB can be recovered from backup/failover within your RTO

#### Recovery Point Objective (RPO)
- Define the **maximum acceptable data loss** during an incident
- RPO indicates how frequently backups must be taken (e.g., RPO of 15 minutes = backup every 15 minutes)
- **CMDB RPO**: Ensure CMDB backups are taken at frequency matching your RPO

#### Document and Test Recovery Objectives
- Document MTID, RTO, and RPO for all critical functions and systems (including CMDB)
- Regularly test recovery procedures to verify targets can be achieved
- Conduct business continuity drills at least annually
- Update recovery objectives based on changes in operations or threats

### 5. Advanced Threat-Led Penetration Testing (TLPT) - Mandatory

DORA requires **sophisticated, adversary-informed penetration testing** conducted annually:

#### What Is TLPT?
- **Threat-led penetration testing**: Realistic, adversary-informed simulated attacks designed to identify vulnerabilities and test defenses
- Not basic network vulnerability scans; TLPT is sophisticated, targeted attack simulation
- Conducted by specialized red teams (internal or external) with deep security expertise

#### TLPT Scope
- **Must test critical systems**, including CMDB if it is critical
- Test real attack scenarios relevant to your institution (not generic tests)
- Test technical controls (firewalls, detection systems, access controls, encryption)
- Test organizational controls (incident response processes, communication, recovery procedures)
- Test human factors (phishing awareness, social engineering resistance)

#### TLPT Frequency and Requirements
- **Annually required** (at minimum)
- Can be conducted in-house (if you have sufficient expertise) or externally contracted
- If external, must be conducted by independent, qualified third-party
- Results must be documented and reported to the board

#### TLPT for CMDB
- Test CMDB security controls:
  - Can testers bypass access controls and gain unauthorized access?
  - Can testers modify CMDB data and go undetected?
  - Can testers exfiltrate sensitive configuration data?
  - Can testers disrupt CMDB availability?
  - How long until incident is detected?
  - How effective is incident response?
- Simulate real attack scenarios (ransomware, insider threat, supply chain attack)
- Test recovery procedures to verify CMDB can be recovered within RTO

### 6. ICT Third-Party Risk Management (Mandatory)

DORA imposes explicit requirements for managing critical vendors and service providers:

#### Identify Critical Third Parties
- Identify vendors and service providers **critical to your ICT operations**
- Examples for CMDB: CMDB software vendor, hosting provider, managed service provider, security tool vendors
- Critical = if the vendor fails, your operations are significantly disrupted and recovery would be difficult

#### Assess Critical Third-Party Security and Resilience
- Evaluate cybersecurity controls of critical vendors
- Assess their ICT risk management practices
- Verify they have incident detection and response capabilities
- Assess their own supply chain security (vendors of vendors)
- Conduct due diligence and periodic audits

#### Contractual Requirements with Critical Third Parties
- Require vendors to comply with DORA principles (even if not directly regulated)
- Require vendors to notify you of security incidents within **24 hours** of detection
- Include audit rights (right to inspect vendor ICT controls)
- Include incident reporting obligations and escalation procedures
- Define security incident thresholds requiring escalation to your board
- Include liability clauses for security failures and availability breaches
- Require vendors to maintain insurance for cyber liability

#### Manage Vendor Changes and Continuity
- Monitor for changes in critical vendors (acquisition, bankruptcy, policy changes)
- Assess impact of vendor changes on your operational resilience
- Maintain contingency plans for vendor failure (alternative suppliers, backup systems, exit strategies)
- Ensure you can migrate away
