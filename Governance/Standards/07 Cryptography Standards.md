---
standard_ID: "S07"
title: "Cryptography Standards"
status: "Approved"
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approval: "20250903"
next_review: "20260903"
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

#### 3.2.1 Key Rotation Protocols
- Keys must be rotated based on defined cryptoperiods, aligned with NIST SP 800-57 Part 1 and SP 800-175B guidance.
- Rotation must be automated where feasible, with audit logs capturing rotation events and associated metadata.
- Cryptoperiods must be shortened for high-sensitivity data or exposed trust boundaries.

#### 3.2.2 Key Lifecycle Enforcement
- Keys must be tagged with lifecycle metadata: creation date, expiration, usage scope, and rotation history.
- Expired or compromised keys must be revoked immediately and replaced with new keys using secure generation protocols.

#### 3.2.3 Personal Key Usage
- Personal cryptographic keys (e.g., contributor signing keys) must be unique, traceable, and stored in secure enclaves or hardware tokens.
- Contributors must not reuse personal keys across environments or roles.
- Personal keys must be rotated annually or upon role change, with attestation logged in contributor onboarding records.

### 3.3 Data Protection 

#### 3.3.1 Data at Rest
- All sensitive data at rest must be encrypted
- Encryption keys must be managed securely, with access restricted to authorized personnel only.
- Regularly rotate encryption keys and audit key usage.

#### 3.3.2 Data in Transit
- All data transmitted over public or untrusted networks must use TLS 1.2 or higher.
- Disable insecure protocols (e.g., SSL, TLS 1.0/1.1).
- Validate certificates and reject expired or self-signed certificates in production systems.

#### 3.3.3 Data in Use
- All data viewed or processed will be subject to role-specific access.
- Data for viewing or processing will be removed when no longer needed or after a 10 minute inactivity period.
- Changes to data shall be logged

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

### 3.8 Implementation Standards

#### 3.8.1 Cryptographic Module Validation
- All cryptographic implementations must use FIPS 140-3 validated modules.
- Contributors must verify module validation status prior to deployment and document it in implementation artifacts.

#### 3.8.2 Approved Mechanism Mapping
- Contributors must select cryptographic mechanisms based on NIST SP 800-175B-approved categories:
  - Data-at-rest: AES-256 with GCM or CBC
  - Data-in-transit: TLS 1.3 with forward secrecy
  - Authentication: HMAC-SHA-256 or digital signatures (RSA/ECC)
  - Integrity: SHA-2 family with MAC or signature verification

#### 3.8.3 Implementation Traceability
- Each cryptographic control must be traceable to a control ID, mechanism type, and contributor attestation.
- Tags (e.g., AES256-GCM, RSA-SIG) must be used in documentation and commit messages to reinforce clarity and auditability.

### 3.9 Contributor Key Stewardship

#### 3.9.1 Contributor Signing Keys
- All contributors must use personal signing keys for commits, attestations, and sensitive operations.
- Keys must be registered during onboarding and validated annually.
- Signing events must include symbolic tags and commit metadata for traceability.

#### 3.9.2 Key Revocation and Recovery
- Contributors must report suspected key compromise immediately.
- Revocation procedures must include automated alerts, access revocation, and issuance of new keys.
- Recovery rituals must include contributor reflection, attestation, and symbolic recommitment to stewardship.

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


