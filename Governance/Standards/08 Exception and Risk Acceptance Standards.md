---
standard_ID: "S08"
title: "Exception Handling for Internal Controls over Secure Development"
status: "Approved"
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approval: "20250903"
next_review: "20260903"
---

# Exception Handling for Internal Controls over Secure Development

## 1. Purpose & Scope

### 1.1 Purpose
This standard defines the required actions, documentation, and approval pathways for identifying, assessing, and resolving exceptions to FinApp’s Internal Controls over Secure Development (ICSD). Rooted in PCAOB Auditing Standard No. 5 (AS5), it ensures that all deviations from secure development controls are traceable, risk-assessed, and approved through formal stewardship channels. Exceptions are treated as symbolic signals of potential exposure and require contributor reflection and auditor review.

### 1.2 Scope
Applies to all contributors, auditors, and project leads involved in secure development activities across FinApp systems, pipelines, and repositories. Covers exceptions to control activities such as code reviews, static analysis, dependency scanning, and secure commit hygiene.

## 2. Roles & Responsibilities

| Role            | Responsibilities                                                                 |
|-----------------|-----------------------------------------------------------------------------------|
| Owner           | Reviews and approves documented exceptions. Ensures alignment with ICSD standards. |
| Contributors    | Identify and escalate exceptions. Complete risk assessments and remediation plans. |
| Auditors        | Document noted exceptions. Validate risk assessments and trace control impact.     |
| Project Lead    | May approve exceptions when audit leads are unavailable. Ensures operational continuity. |

## 3. Standard Requirements

### 3.1 Exception Identification
- Contributors must flag any deviation from secure development controls (e.g., skipped code review, failed scan, unpatched dependency).
- Exceptions must be documented within 24 hours of discovery using the approved ICSD Exception Log format.

### 3.2 Risk Assessment
- All exceptions must undergo a formal risk assessment using the methodology defined in internal document `06 Risk Assessment Standards.md`.
- Risk assessments must include likelihood, impact, control gap analysis, and proposed mitigation.

### 3.3 Approval Workflow
- Exceptions must be reviewed and approved by the Audit Lead or Project Lead prior to deployment or release.
- Emergency exceptions may be temporarily approved but must be retroactively documented and reviewed within 72 hours.

### 3.4 Auditor Documentation
- Auditors must maintain a log of all noted exceptions, including contributor name, control ID, risk rating, and approval status.
- Auditor logs are subject to quarterly review and must be traceable to signed commits or contributor attestations.

## 4. Implementation Guidance

- Use control IDs to tag exceptions 
- Embed exception rituals into contributor onboarding and retrospectives
- Link exception logs to Git commit hashes and contributor checklists

## 5. Exceptions

- Exceptions to this standard must be documented, risk-assessed, and approved using the same workflow.
- Reviewed annually or upon significant changes to secure development protocols.

## 6. Review & Maintenance

- Reviewed annually or upon updates to AS5, NIST SP 800-218, or internal ICSD standards.

## 7. References

- PCAOB AS5 (AS 2201) – Audit Standard for Internal Control Evaluation  
- NIST SP 800-218 – Secure Software Development Framework (SSDF)  
- Internal Document: `06 Risk Assessment Standards.md`  
- OWASP SAMM / ASVS for secure development maturity modeling

## 8. Audit & Traceability

- Compliance verified through periodic review of exception logs, risk assessments, and approval records.
- Contributors may be asked to attest to exception handling via signed commits or symbolic stewardship checklists.

---

## Appendix

### A. Definitions

| Term         | Definition                                                                 |
|--------------|-----------------------------------------------------------------------------|
| ICSD         | Internal Controls over Secure Development                                   |
| Exception    | A documented deviation from an expected control activity                    |
| Risk Rating  | Quantified assessment of likelihood and impact based on internal standards  |

### B. Version History

Version history tracked via Git commit log.
