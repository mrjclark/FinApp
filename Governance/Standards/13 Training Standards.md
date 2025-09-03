---
standard_ID: "S13"
title: "Training Standards"
status: "Draft"
document_owner: ""
document_maintainer: ""
last_approval: "YYYYMMDD"
next_review: "YYYYMMDD"
---

# Training Standards

## 1. Purpose & Scope

### 1.1 Purpose
This standard defines the minimum training requirements for all FinApp contributors, ensuring alignment with secure development practices, regulatory expectations, and stewardship principles. It reflects guidance from NIST, OWASP, and internal governance to foster a culture of awareness, resilience, and traceable compliance.

### 1.2 Scope
Applies to all FinApp systems, environments, and personnel—including developers, analysts, product managers, and executive stewards. Training modules are tailored by role and mapped to control IDs for audit traceability.

## 2. Roles & Responsibilities

| Role              | Responsibilities                                                                 |
|-------------------|----------------------------------------------------------------------------------|
| Owner             | Defines training scope, approves exceptions, and ensures alignment with standards |
| Contributors      | Completes assigned training, escalates gaps, and attests to adherence             |
| Maintainers       | Updates training modules, tracks completion, and integrates feedback              |
| Auditors          | Reviews training logs and validates control alignment                             |

## 3. Standard Requirements

### 3.1 Security Awareness and Training
- All personnel must complete security awareness training annually.
- Training must include secure development practices, data protection, incident reporting, and phishing resistance.
- Completion must be documented and traceable.

### 3.2 Role-Based Training Modules
- Developers: OWASP Proactive Controls, ASVS Level 1–2, secure SDLC practices.
- Analysts: Threat modeling, incident response protocols (NIST CSF Respond/Detect).
- Product Managers: Privacy-by-design, risk awareness, contributor onboarding.
- Executives: Governance, regulatory alignment (SOX, GDPR), symbolic stewardship modeling.

### 3.3 Contributor Attestation
- Contributors must attest to training completion via signed commits.
- Attestations are stored in audit logs and reviewed quarterly.

### 3.4 Continuous Improvement
- Training content is reviewed annually or upon major control updates.
- Feedback loops are embedded to refine modules and reinforce emotional stewardship.

## 4. Implementation Guidance

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved by the standard owner.
- Reviewed annually and tied to compensating controls.

## 6. Review & Maintenance
- Reviewed annually or upon significant regulatory or operational changes.
- Maintainers update modules and symbolic tags as needed.

## 7. References
- NIST SP 800-50, SP 800-16, SP 800-181, SP 800-53 AT-2
- OWASP ASVS, Proactive Controls, Secure Coding Practices Guide
- ISO/IEC 27001:2022, 27701

## 8. Audit & Traceability
- Compliance verified through periodic review of training logs, contributor attestations, and onboarding artifacts.

---

## Appendix

### A. Definitions

| Term              | Definition                                                                 |
|-------------------|----------------------------------------------------------------------------|
| ASVS              | Application Security Verification Standard (OWASP)                         |
| AT-2              | NIST control for security awareness and training                           |

### B. Version History
Version history tracked via Git commit log.
