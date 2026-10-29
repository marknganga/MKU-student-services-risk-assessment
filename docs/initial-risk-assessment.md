# Initial Cybersecurity Risk Assessment
## Mount Kenya University: Thika Main Campus student services case study

**Prepared by:** Mark Nganga  
**Date:** 29 October 2026  
**Version:** 1.0  
**Classification:** Public educational portfolio project  
**Status:** Preliminary, scenario-based desktop assessment; not an institutional audit

> Independent learning exercise. This project was not commissioned, approved, or endorsed by Mount Kenya University (MKU). It contains no verified security vulnerabilities, private student information, or claims of an actual breach. Ratings describe explicitly assumed conditions, not MKU's measured security posture.

## 1. Executive summary

This assessment examines potential risks affecting student services used by the Thika Main Campus community. It focuses on portal accounts, academic and fee information, historical hostel building reservations, and a conditional extension for disciplinary records. The purpose is to demonstrate asset identification, risk analysis, prioritization, and practical treatment planning.

Evidence consists of publicly available MKU information and the preparer's recollection of hostel bookings. Students historically selected a general hostel building through the portal; individual room selection was not recalled as an available function. The ability to amend or cancel reservations is unknown. Disciplinary records were suggested as an asset, but their system of record and relationship to the portal have not been established.

Six illustrative scenarios are assessed under stated assumptions: phishing, misuse of staff privileges, accommodation information disclosure, service outage, destructive malware, and disciplinary information disclosure. Four scenarios receive a High illustrative score and two receive Medium. These counts describe the model only. They do not establish four high risks at MKU.

The immediate recommendation for any real follow-up is to verify scope and existing controls with authorized system owners. Depending on that evidence, priority actions could include stronger account authentication and recovery, least-privilege access, monitoring of sensitive changes, tested restoration, and service continuity planning. No institutional residual risk or overall security rating can be concluded from this exercise.

## 2. Organization and assessment purpose

MKU identifies its main campus as being along General Kago Road, Thika [S1]. Its public student services page links to digital services and advises users to safeguard passwords and log out after using shared facilities [S2]. Its public digital gateway describes access to registration, results, fee statements, learning services, and other functions [S3]. These descriptions establish context; they do not disclose the technical architecture or effectiveness of security controls.

The assessment asks: what could interrupt student services, expose private records, or undermine the accuracy of university information? It translates technical scenarios into effects on students and administrative work.

## 3. Scope and boundaries

**Core scope:** Student portal account access and student-facing academic and fee information; hostel building reservations as a historical workflow requiring current confirmation.

**Conditional scope:** Disciplinary records, assessed as a separate student-records scenario only. Inclusion does not imply they are stored in or accessible through the student portal.

**Perspective:** Users and services associated with Thika Main Campus. The portal may serve multiple campuses. Hosting location, ownership boundaries, shared infrastructure, and providers are unknown.

**Excluded:** Network penetration testing, vulnerability scanning, credential testing, real student records, payment-provider infrastructure, research systems, healthcare records, and a full university-wide or compliance audit. No authenticated system access, staff interviews, configuration reviews, or technical tests were performed. Public pages alone cannot establish an absence of controls.

## 4. Evidence, assumptions, and uncertainty

| ID | Basis | Observation or limitation |
|---|---|---|
| E1 | Official public page, S1 | Main campus location in Thika confirmed; infrastructure boundaries not established. |
| E2 | Official public page, S2 | Student digital service links and public password/logout advice exist. Advice alone does not prove staff training or technical enforcement. |
| E3 | Official public gateway, S3 | Portal functions described publicly include registration, results and fees. Public descriptions may change and are not architecture documentation. |
| E4 | Preparer's historical recollection | Students reserved a general hostel building through the portal; no individual room selection recalled. Date and current workflow unverified. |
| E5 | Preparer's proposed asset | Disciplinary records are a candidate asset. Storage, access route and portal integration are unverified. |
| A1 | Scenario assumption | A stolen credential could be used if authentication or recovery safeguards are insufficient. Actual MFA and recovery controls unknown. |
| A2 | Scenario assumption | Excessive access or inadequate review could permit misuse. Actual role permissions and audit capabilities unknown. |
| A3 | Scenario assumption | Availability or recovery weaknesses could extend an outage. Actual redundancy, capacity and backups unknown. |

All scenario scores have **low evidence confidence**. Public facts and recollections support context, not the presence of exploitable weaknesses. Unknowns remain unknown; assumptions are not findings.

## 5. Asset inventory

Information fields below are examples for analysis and must be confirmed. C = confidentiality, I = integrity, A = availability.

| ID | Asset | Value and potential consequences | Primary security objectives | Status |
|---|---|---|---|---|
| AS1 | Student and staff portal accounts | Control access to services and personal information; compromise can enable impersonation. | C, I | Portal exists; account architecture unknown |
| AS2 | Academic records | Incorrect results or registration data could affect progression and require correction. | I, C, A | Publicly described function |
| AS3 | Fee statements | Incorrect or unavailable balances could disrupt reconciliation or student processes. | I, C, A | Publicly described function; no payment-processing architecture assumed |
| AS4 | Hostel building reservation records | May connect student identity to a selected building and booking status; disclosure affects privacy. | C, I, A | Historical recollection; fields and current process unconfirmed |
| AS5 | Disciplinary records | Potentially include allegations, outcomes and appeals; disclosure or alteration could cause serious personal harm. | C, I | Conditional asset; content and location unconfirmed |
| AS6 | Student portal service | Supports access to registration and records; outage can delay student and staff work. | A, I | Publicly described service; dependencies unknown |

Proposed stakeholders for verification include ICT service owners, registry, finance, accommodation services and student affairs. These are functional roles, not confirmed MKU ownership assignments.

## 6. Methodology and scoring

This is a simplified qualitative exercise informed by the risk-assessment concepts in NIST SP 800-30 Rev. 1 [S4]. It is not a full application of that publication or a claim of certification. Each scenario links an asset, threat event, enabling condition, and consequence. Existing protections must be established before institution-specific likelihood can be estimated.

For this exercise only, use a **12-month planning horizon** and an ordinal score: **likelihood × impact**. The product is a prioritization aid, not a numerical probability or financial loss estimate.

| Score | Likelihood under the stated assumptions | Impact if the scenario occurs |
|---|---|---|
| 1 | Low: substantial barriers or limited exposure in the assumed case | Low: localized inconvenience, routine recovery, little sensitive information affected |
| 2 | Medium: plausible event with meaningful uncertainty | Medium: material disruption or limited private information exposure, requiring coordinated correction |
| 3 | High: readily attempted event and weak assumed barriers | High: serious private information exposure, material loss of record integrity, or prolonged disruption to critical student processes |

**Bands:** 1–2 Low; 3–4 Medium; 6–9 High. Only 1, 2, 3, 4, 6 and 9 can result. For multi-dimensional impact, use the highest reasonably justified consequence rather than adding scores.

Scores below are **illustrative scenario scores under assumed insufficient safeguards**. They are neither verified current risk nor strictly control-free inherent risk. Actual current and residual ratings are pending evidence. Where impact or likelihood is uncertain, the narrative states why the example score was chosen.

## 7. Risk register

| ID | Scenario and assumed enabling condition | L | I | Score | Rationale |
|---|---|---:|---:|---|---|
| R1 | Phishing captures a portal user's credentials; assume no effective additional authentication or recovery barrier, permitting unauthorized access. | 3 | 3 | 9 High | Phishing is readily attempted; sensitive access could cause significant harm. Actual protections and accessible functions are unknown. |
| R2 | A compromised or misused staff account changes academic or fee records; assume excessive edit rights and insufficient approval or change review. | 2 | 3 | 6 High | Requires appropriate access, so likelihood is Medium in this model; altered records could seriously affect students and reconciliation. |
| R3 | An unauthorized user views another student's hostel building reservation; assume inadequate authorization checks or excessive viewing rights. | 2 | 2 | 4 Medium | Assume limited disclosure affecting a small number of students. Building association could expose accommodation information; targeted safety concerns could raise impact. |
| R4 | A demand surge or dependency failure makes the portal unavailable during registration; assume inadequate capacity, resilience or fallback arrangements. | 2 | 2 | 4 Medium | Assume a short outage recoverable within a day with extensions available. Longer outage or missed deadlines could raise impact to High. |
| R5 | Destructive malware affects a supporting administrative environment; assume it can reach relevant records and recovery copies are unavailable or untested. | 2 | 3 | 6 High | Depends on unknown architecture. Under the assumed condition, prolonged service loss and inability to recover records justify High impact. |
| R6 | An unauthorized staff member or external recipient receives disciplinary information; assume excessive access or an insecure export/sharing process. | 2 | 3 | 6 High | Conditional on the asset being in scope. Sensitive allegations or outcomes could cause serious privacy and reputational harm. No portal connection assumed. |

**Existing safeguards:** E2 confirms public password and logout advice. MFA, authorization, privileged access, logging, resilience, malware protection, backups and records-sharing procedures remain unverified. None of the six scenarios is a confirmed vulnerability.

## 8. Treatment recommendations and validation

All responses below propose mitigation. An authorized owner would determine whether to mitigate, accept, transfer or avoid a risk after reviewing evidence. Proposed roles and completion windows are illustrative and start only after an agreed real assessment kickoff; they are not commitments by MKU.

| Risk | Proposed treatment if a gap is confirmed | Proposed accountable function | Window | Evidence of completion |
|---|---|---|---|---|
| R1 | Prioritize phishing-resistant MFA for privileged users; extend appropriate MFA to users, secure recovery, revoke compromised sessions, and teach verification of suspicious messages. | ICT identity/service owner | 0–30 days for priority account review and plan | Approved configuration evidence and authorized authentication/recovery checks using test accounts |
| R2 | Apply least privilege, named staff accounts, approval for sensitive changes, access reviews and protected audit logs. | Registry/finance record owner with ICT | 0–30 days for review; remediation plan by day 60 | Role matrix, approved access review, and test change showing actor, time, old/new value and approval |
| R3 | Confirm hostel workflow; restrict records to the student and authorized staff; enforce server-side authorization and review access logs. | Accommodation records owner with ICT | Verify within 30 days | Approved access matrix and authorized synthetic-account check confirming cross-student access is denied |
| R4 | Define availability objectives, monitor service health, plan capacity, publish fallback and deadline-extension procedures. | Portal service owner with registry | 30–60 days | Agreed service objectives and an approved continuity exercise; load testing only in an authorized environment |
| R5 | Protect endpoints, reduce administrative privileges, separate recovery copies, set recovery objectives and perform isolated restoration exercises. | ICT operations and service owner | 30–60 days | Documented successful restore, recovered-record verification and measured recovery time/data loss against agreed objectives |
| R6 | Identify the system of record, restrict case access, approve secure sharing, review exports and define appropriate retention. | Student affairs/disciplinary records owner with privacy function | Scope check within 30 days; plan by day 60 | Approved data flow, permissions review and synthetic sharing exercise showing authorized recipients only |

Controls should be verified before adding duplicates. Retaining logs or backups also requires appropriate access restrictions and retention decisions. No legal compliance conclusion is made here.

## 9. Action plan and monitoring

**Days 0–30: establish facts.** Confirm services and owners, hostel functionality, disciplinary scope, account protections and current incident procedures. Review high-impact account and data-access scenarios first. Record evidence references without publishing private configurations.

**Days 31–60: address confirmed gaps.** Agree remediation owners, implement prioritized changes, test recovery and continuity, and validate access boundaries using approved test data.

**Days 61–90: reassess.** Confirm completion evidence, re-score scenarios using actual controls, and obtain explicit owner decisions for remaining exposure. Review after a major system change or relevant incident and at an agreed periodic interval.

Suggested measures: percentage of privileged accounts with strong MFA; overdue access reviews; percentage of sensitive changes with complete audit evidence; successful restore exercises against objectives; and unresolved high risks. Baselines and targets must be agreed; this report contains no measured results.

**Residual risk:** Not assessed. A recommendation does not prove a control exists or works. Re-score likelihood and impact only after validating implementation. Some privacy impacts may remain High even when likelihood falls. Institutional risk acceptance belongs to authorized management, not the portfolio author.

## 10. Questions for an authorized follow-up

1. Which student services currently serve Thika users, and who owns each system and dataset?
2. Does hostel building booking still occur through the portal? What fields are visible to each role? Can bookings be changed or cancelled?
3. Where are disciplinary records stored, and do they have any portal integration? If separate, should they be removed from a portal-only assessment?
4. What MFA, password recovery, session handling and account removal arrangements are implemented?
5. Which staff can change academic and fee records, and what approval and audit mechanisms apply?
6. What are the recovery time objective (RTO: maximum acceptable restoration time) and recovery point objective (RPO: maximum acceptable data loss measured in time)? When was restoration last demonstrated?
7. What service dependencies, capacity arrangements, escalation routes and continuity procedures apply?
8. What incident and availability evidence can owners provide in an appropriately redacted form?

## 11. Conclusion

This preliminary exercise identifies plausible risk scenarios and a structured route to validating them. It does not establish that MKU lacks controls or has suffered an incident. The strongest next step is evidence gathering with authorized owners, followed by assessment of actual controls and agreed treatment of confirmed risks.

## 12. Sources

Public sources reviewed on 29 October 2026. They establish context, not security findings; some university pages may describe older workflows.

- **S1:** Mount Kenya University, Thika Main Campus. https://mku.ac.ke/thika-main-campus/
- **S2:** Mount Kenya University, Student Services. https://mku.ac.ke/student-services/
- **S3:** Mount Kenya University Digital Ecosystem. https://portal.mku.ac.ke/ — reviewed during project research on 28 October 2026; features should be reconfirmed for operational use.
- **S4:** NIST SP 800-30 Rev. 1, Guide for Conducting Risk Assessments. https://csrc.nist.gov/pubs/sp/800/30/r1/final
- **S5:** Preparer's recollection supplied during this project: building-level hostel booking through the student portal; changes/cancellation not recalled. Historical, not independently verified.
