---
standard_ID: "S03"
title: "Data Classification Standard"
status: "Approved"
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approval: "20250903"
next_review: "20260903"
---

# Data Classification Standard

## 1. Purpose & Scope

### 1.1 Purpose
This standard establishes symbolic tiers of data classification to protect FinApp information assets in alignment with NIST IR 8496. It is created to ensure persistent labeling of data across systems and environments, risk‑informed handling procedures mapped to classification tiers, and clear contributor stewardship obligations and audit‑ready traceability.

### 1.2 Scope
Applies to all contributors, contractors, and third‑party service providers who create, access, process, transmit, store, or dispose of FinApp data, including application source code and configuration files, customer and operational data, audit logs, security event records, and compliance documentation, and physical and digital media should FinApp ever contain any

## 2. Roles & Responsibilities

| Role                  | Responsibilities |
|-----------------------|------------------|
| Data Owner        | Defines classification of owned data assets; approves classification changes |
| Data Steward      | Ensures labels are applied, persistent, and reviewed; trains contributors |
| Contributors      | Correctly label and handle data per classification; report deviations |
| Security Team     | Monitors compliance, maps controls to classifications, conducts audits |

## 3. Standard Requirements

### 3.1 Classification Tiers
All data assets must be assigned one of the following tiers at creation:

| Tier         | Description | Attributes (per IR 8496) | Examples |
|--------------|-------------|---------------------------|----------|
| Public   | Approved for release to anyone | Low sensitivity, low criticality, low confidentiality | Marketing website content |
| Internal | FinApp use only, non‑public | Moderate sensitivity; limited business impact if disclosed | Internal process docs |
| Confidential | Sensitive; restricted to authorized roles | High sensitivity, moderate‑high criticality; may trigger compliance obligations | Customer PII or PFI |
| Restricted | Critical; severe impact if compromised | Very high sensitivity, criticality, and confidentiality | Encryption keys, security configs |

### 3.2 Labeling & Persistence
- Classification labels must persist across storage, processing, and transmission
- Labels must be machine‑readable and human‑interpretable
- Labels may be embedded in file metadata, database schemas, or application UI indicators
- Labels must not be removed or altered without Data Owner approval

### 3.3 Handling & Access Controls
- Access to Confidential or higher data requires role‑based access control (RBAC) and MFA
- Confidential or higher data will use hardware based protections when it is in processing
- Confidential or higher data must initially be rendered in a masked state when being viewed
- Restricted data must be encrypted in transit (TLS 1.2+) and at rest (AES‑256 or equivalent)
- Data handling procedures must follow least privilege principles
- Access logs for Confidential or higher must be reviewed quarterly

### 3.4 Review & Reclassification
- Classifications must be reviewed at least annually or upon significant data changes
- Downgrading classification requires documented risk assessment and Security Team approval
- Expired or obsolete data should be securely disposed of per retention schedule

## 4. Implementation Guidance
- Integrate classification into CI/CD pipelines for automated labeling
- Use data discovery tools to identify unlabeled assets
- Align classification with Zero‑Trust principles

## 5. Exceptions
- All exceptions must be documented in the Exception Register with risk assessment
- Exceptions require approval from both Data Owner and Security Lead
- Exceptions reviewed annually

## 6. Review & Maintenance
- Reviewed annually or upon major system or regulatory changes
- Maintained in Git for full version history and traceability

## 7. References
- NIST IR 8496 – Data Classification Concepts and Considerations
- NIST SP 1800‑39 – Implementing Data Classification Practices
- NIST SP 800‑53 – Security and Privacy Controls
- S01 Access Control Standard

## 8. Audit & Traceability
- Compliance verified through sampling of labeled assets and review of handling logs
- Contributors attest via onboarding checklists and quarterly compliance confirmations

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Data Classification | The process of categorizing data based on sensitivity, criticality, and confidentiality |
| Persistent Labeling | Labeling that remains with data across its lifecycle and storage/transmission contexts |
| Data Steward | Individual responsible for ensuring ongoing accuracy and persistence of classification labels |

### B. Version History
Tracked via Git commit log.
