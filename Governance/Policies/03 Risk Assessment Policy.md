---
policy_ID: "P03"
title: "Risk Assessment Policy"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# Risk Assessment Policy

## 1. Purpose & Scope

### 1.1 Purpose
To establish a consistent and effective approach for identifying, assessing, treating, and monitoring information security risks throughout the FinApp project lifecycle, in line with NIST Risk Management Framework (RMF) requirements, as well as the implementation of NIST SP 800-53 controls to support risk assessments.

### 1.2 Scope
This policy applies to all information assets, technology components, development activities, and supporting processes within the FinApp project.

## 2. Policy Statement
FinApp is committed to proactively identifying and managing risks that may impact the confidentiality, integrity, and availability of its information assets and services. Risk assessment is integral to the secure software development lifecycle and ongoing project management.

## 3. Policy Objectives
- Ensure consistent identification and assessment of information security risks.
- Support informed decision-making for risk treatment and control selection.
- Maintain compliance with NIST RMF and NIST SP 800-53 requirements.
- Protect the confidentiality, integrity, and availability of information assets.
- Promote continual improvement of risk management practices.

## 4. Roles and Responsibilities

### 4.1 Key Roles
| Role | Responsibilities |
| --- | --- |
| Project Lead (Owner, System Owner, Authorizing Official) | Accountable for policy creation, review, and enforcement. Approves risk acceptance and ensures adequate resources for security. Oversees system development and authorization decisions. |
| Contributors (System Security Engineers, Users) | Execute secure development tasks. Follow security policies and report anomalies. Participate in training and implement assigned controls. |
| Reviewers/Auditors (Security Control Assessors) | Independently assess controls, review audit logs, and report deficiencies. Support authorization decisions and continuous improvement. |
| Third Parties (External Providers, Common Control Providers) | Deliver services or components under agreed security requirements. Participate in supply chain reviews and maintain inherited controls. |

## 5. Risk Assessment Requirements
- The project must: 
    - Create risk assessments following best industry practices.
    - Create and maintain a System Security Plan (SSP) for all systems developed.
    - Create a Security Plan of Action and Milestones (SPOA&M) for any security control that is implemented. This plan must be updated when a risk assessment is amended.
    - Create and maintain a Privacy Plan with specific security objectives on protecting PII and PFI.:

## 6. Reporting and Escalation
- All identified risks and treatment decisions are documented.
- Security incidents or new significant risks are reported to the project owner for review and response.

## 7. Policy Review
- This policy is reviewed annually or following significant changes to the project or threat landscape.

## 8. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 9. Review & Maintenance
* Reviewed annually or upon significant changes.

## 10. References
- [NIST RMF](https://csrc.nist.gov/Projects/Risk-Management)
- [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [NIST SP 800-53B](https://csrc.nist.gov/publications/detail/sp/800-53b/final)
- [NIST SP 800-60](https://csrc.nist.gov/publications/detail/sp/800-60/rev-1/final)
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)

---

## Appendix

### A. Definitions
| Term | Definition |
|---|---|
| Risk Management Framework (RMF) | A structured process for managing security and privacy risk that integrates with the system development life cycle. |
| System Security Plan (SSP) | A formal document that describes the security controls in place or planned for an information system. |
| Security Assessment Report (SAR) | A report detailing the results of assessing the effectiveness of security controls. |
| Plan of Action and Milestones (POA&M) | A document identifying tasks to correct deficiencies and reduce or eliminate vulnerabilities. |
| Privacy Plan | A document outlining privacy controls and how they are implemented to protect personally identifiable information (PII). |
| Categorization | The process of determining the impact level of a system based on the sensitivity of the information it processes. |

### B. Version History
Version history is maintained in the Git commit log.
