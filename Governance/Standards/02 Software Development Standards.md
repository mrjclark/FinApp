---
document_ID: "S02"
title: "Software Development Standards"
status: "Draft"                # Options: Draft, Approved, Deprecated
document_owner: ""
document_maintainer: ""
last_approved: "YYYYMMDD"
next_review: "YYYYMMDD"
---
# Software Development Standards

## 1. Purpose & Scope

### 1.1 Purpose
This document is to set the minimum required precautions to be taken to ensure that development of the software is done to ensure the confidentiality and integrity of the project goals.

### 1.2 Scope
These standards apply to all systems, applications, and personnel handling or accessing sensitive data within the organization.

## 2. Roles & Responsibilities
| Role | Responsibilities |
| --- | --- |
| Owner (Project Lead) | Responsible for establishing standards, enforcing compliance, approving exceptions, and documenting exceptions with their compensating controls |
| Contributors | Responsible for tasks as given by the project lead. Reports to the project lead or documented delegate. |

## 3. Secure Development Standards

###  Supply Chain Management
- A process will be established to ensure that all third party assets (TPA) are controlled. Any vulnerabilities that are inherent in the TPA will be identified. Controls will be put into place to ensure that risks due to TPA's are reduced.
- All TPA's will require to undergo a scrutinization process before implementation to ensure that the security and privacy needs of the project are met. Origin, integrity, and supplier claims must be tested and confirmed. 
- FinApp design must tolerate any supplier failure or compromise.
- Every release must include a validated SBOM. Any vulnerabilities arising from TPA's must be tracked and remediated within one (1) week. Affected releases will be pulled if any vulnerabilities from TPA's that are known to be exploited outside of research.

###  Developer Access Control Management
All access control as per the S01 Access Control Implementation Standards.md are still applicable. If excess, the following access standards are implemented to any individual who will have access to development environments.
- Developers will have specific access to view, modify, and remove portions of the code base and workflows related to their codein non-production environments and branches. 
- Access to specific files will be role based. 
- No other role will have direct access to code base.
- Role authorization will be granted by a Development Lead or Project Lead.
- Developers will not have access to modify access levels of their own or other roles, project security objects, or governance.
- Developers will not have access to modify or remove code or workflows from the production environment or branch.
- Developer commits will need to be verified.
- Developer access will be removed per Human Resources Standards.

### Securing Sensitive Data
Data classified as sensitive as per the SXX Data Classification Standards.md will have the following additional standards applied:
- All sensitive data transference within FinApp will be logged in an auditable, immutable, local and centralized area.
- All sensitive data will have cryptographic measures applied when leaving the bounds of FinApp.
- All data flows will be explicitly authorized and constrained by design. This will be done by identifying trust zone, establishing flow control designs between zones, and require boundary enforcement mechanisms.
- Regular scanning for API key's, authorization token, environment secrets, and project contributor PII will be performed. Upon detection, the Project Lead and DevSecOps Lead will be notified. Any releases containing this information will be pulled until all information leakage has been handled.

###  insider_control_bypass:
    sp800-53: [PM-12, AC-5, AC-6, AU-6]
    sp800-218: [PO, PS]
    sp800-160: [human_factors_controls, traceability]
###  exploiting_exposed_systems:
    sp800-53: [SC-7, RA-5, SI-4, CM-8]
    sp800-218: [PW, PS]
    sp800-160: [boundary_resilience, verification]
###  dos_on_contributor_infra:
    sp800-53: [SC-5, CP-2, CP-4]
    sp800-218: [PO]
    sp800-160: [availability_resilience, testing]
###  recently_discovered_vulns:
    sp800-53: [RA-5, SI-2, CA-7, IR-4]
    sp800-218: [RV]
    sp800-160: [continuous_risk_treatment, nonconformance_management]

## 4. Implementation Guidance
[Optional section for best practices, tooling suggestions, or links to procedures.]

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  

## 6. Review & Maintenance
* Reviewed annually or upon significant changes.

## 7. References
- NIST [Relevant Publications]  
- OWASP / CIS / Additional frameworks  
- Internal policy or repo links (if applicable)

## 8. Audit & Traceability
- Compliance is verified through quarterly reviews of implementation artifacts.
- Contributors will be asked to attest to adherence via signed commits or onboarding checklists.

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| {{Term}} | {{Definition}} |

### B. Version History
Version history tracked via Git commit log.
