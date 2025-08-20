---
standard_ID: "S07"
title: "Cryptography Standards"
status: Draft
document_owner: ""
document_maintainer: ""
last_approval: "YYYYMMDD"
next_review: "YYYYMMDD"
---

# Cryptography Standards

## 1. Purpose & Scope

### 1.1 Purpose
To define the minimum cryptographic requirements necessary to protect the confidentiality, integrity, and authenticity of FinApp systems and data. This standard uses NIST SP 800-175A/B as guidance for FinApp’s governance, ensuring contributors uphold trust through approved cryptographic mechanisms.

### 1.2 Scope
Applies to all FinApp systems, services, contributors, and environments where sensitive data is stored, transmitted, or processed. Includes internal APIs, contributor devices, CI/CD pipelines, and third-party integrations.

## 2. Roles & Responsibilities

| Role | Responsibilities |
|------|------------------|
| Owner | Defines and enforces cryptographic standards. Reviews exceptions and approves updates. |
| Contributors | Implement cryptographic controls in alignment with this standard. Escalate deviations or gaps. |
| Auditors | Verify compliance through artifact review and contributor attestation. |

## 3. Standard Requirements

### 3.1 Algorithm Selection 
- Only use algorithms approved by NIST SP 800-175B Rev. 1 (e.g., AES, SHA-2, RSA, ECC).
- Deprecated algorithms (e.g., MD5, SHA-1, DES) are prohibited.

### 3.2 Key Management 
- Keys must be generated, stored, and rotated per NIST SP 800-57 Part 1.
- Keys must be protected using FIPS 140-3 validated modules.
- Cryptoperiods must be defined based on key type and data sensitivity.

### 3.3 Data Protection 
- Sensitive data must be encrypted at rest and in transit using approved algorithms.
- TLS 1.2 or higher must be used for all network communications.
- Encryption keys must not be hardcoded or stored in plaintext.

### 3.4 Authentication & Integrity 
- Use digital signatures or MACs to verify authenticity and integrity of critical data.
- Cryptographic authentication must be used to verify contributor and system identities.

### 3.5 Entropy & Randomness 
- Random number generation must use approved entropy sources.
- Contributors must validate entropy quality during key generation.

### 3.6 Compliance & Validation 
- All cryptographic modules must be FIPS 140-3 validated.
- Contributors must verify module validation status before deployment.

### 3.7 Cryptographic Method Selection 
- Symmetric cryptography (e.g., AES, HMAC) must be used for internal data protection, MACs, and performance-critical operations.
- Asymmetric cryptography (e.g., RSA, ECC) must be used for digital signatures, contributor attestations, and non-repudiable actions.
- Contributors must select methods based on data classification, trust boundaries, and audit requirements.

## 4. Implementation Guidance
- Reference guides for AES key generation, TLS configuration, and entropy validation are maintained in the FinApp Procedures Repository.

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  

## 6. Review & Maintenance
- Reviewed annually or upon significant changes.

## 7. References
- NIST SP 800-175A Rev. 1  
- NIST SP 800-175B Rev. 1  
- NIST SP 800-57 Part 1  
- FIPS 140-3  
- OWASP Cryptographic Storage Cheat Sheet  
- [Cryptography Policy](../Policies/13\ Cryptography\ Policy.md)

## 8. Audit & Traceability
- Compliance verified through periodic review of implementation artifacts.
- Contributors may be asked to attest to adherence via onboarding checklists or signed commits.

---

## Appendix

### A. Definitions

| Term | Definition |
|------|------------|
| Cryptoperiod | The time span during which a cryptographic key is authorized for use. |
| Entropy | Randomness collected by a system for use in cryptographic operations. |
| FIPS-validated module | A cryptographic module that meets the requirements of FIPS 140-3. |
| Message Authentication Codes (MACs) | Provides a way to verify both the integrity and the authenticity of a message using symmetric cryptography. | 

### B. Version History
Version history tracked via Git commit log.


