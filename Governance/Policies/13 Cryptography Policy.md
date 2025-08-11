---
policy_ID: "P13"
title: "Cryptography Policy"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# Cryptography Policy

## 1. Purpose & Scope

### 1.1 Purpose
To define the principles and requirements for the use, management, and protection of cryptographic controls within the FinApp project, ensuring the confidentiality, integrity, and authenticity of information in accordance with ISO/IEC 27001:2022.

### 1.2 Scope
This policy applies to all data, systems, applications, and communications within the FinApp project where cryptographic measures are used to protect information. All project roles are covered.

## 2. Policy Statement
The FinApp project is committed to using appropriate cryptographic controls to protect sensitive and personal information from unauthorized access, modification, or disclosure.

## 3. Policy Objectives
- Apply cryptographic controls to protect data at rest, in transit, in use, and as required by law, regulation, or risk assessment.
- Use only approved cryptographic algorithms, protocols, and key lengths.
- Securely generate, store, distribute, retire, and destroy cryptographic keys.
- Protect private keys and passwords against unauthorized access.
- Regularly review and update cryptographic controls to address emerging threats.
- Implement and document compensating controls where encryption is not feasible.
- Identify and comply with legal, regulatory, and contractual requirements for cryptography.

## 4. Roles & Responsibilities

| Role                                | Responsibility                                                                 |
|-------------------------------------|---------------------------------------------------------------------------------|
| Policy Author                       | Define organizational requirements for cryptographic protection of information. |
| Cryptographic Standards Advisor     | Select approved algorithms and key lengths based on NIST guidance.              |
| Key Management Officer              | Establish procedures for key generation, distribution, storage, and destruction.|
| System Architect                    | Specify use cases for symmetric vs. asymmetric cryptography in system design.   |
| Compliance Officer                  | Ensure use of validated cryptographic modules (e.g., FIPS 140-3 compliant).     |
| Digital Signature Coordinator       | Define procedures for signature creation and verification.                      |
| Identity Authentication Lead        | Implement cryptographic identity mechanisms (e.g., certificates, tokens).       |
| Integrity Assurance Analyst         | Apply MACs and hashing to ensure message integrity.                             |
| Key Establishment Engineer          | Design secure key exchange and agreement protocols.                             |
| Random Bit Generation Steward       | Use approved DRBGs for cryptographic randomness.                                |
| Crypto Agility Planner              | Monitor algorithm lifecycle and plan for transitions (e.g., post-quantum).      |
| Acquisition Manager                 | Integrate cryptographic requirements into procurement and system onboarding.    |

## 5. Cryptography Activities

### 5.1 Cryptographic Governance
- Define organizational requirements for cryptographic protection of sensitive information
- Document roles and responsibilities for cryptographic operations and oversight
- Ensure use of validated cryptographic modules (e.g., FIPS 140-3 compliant)
- Integrate cryptographic controls into system development and acquisition processes
- Align cryptographic policy with FISMA and OMB A-130 requirements

### 5.2 Algorithm and Key Management
- Select approved cryptographic algorithms and key lengths based on NIST standards
- Specify use cases for symmetric vs. asymmetric cryptography
- Establish procedures for key generation, distribution, storage, and destruction
- Plan for algorithm transitions and crypto agility based on NIST guidance

### 5.3 Authentication and Integrity
- Define procedures for digital signature creation and verification
- Establish identity authentication mechanisms using cryptographic methods
- Implement message authentication codes (MACs) for integrity assurance

### 5.4 Key Establishment and Exchange
- Define protocols for secure key establishment and agreement
- Ensure confidentiality and authenticity during key exchange processes

### 5.5 Randomness and Entropy
- Require random bit generation using approved deterministic random bit generators (DRBGs)
- Validate entropy sources and randomness quality for cryptographic operations

## 6. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 7. Review & Maintenance
* Reviewed annually or upon significant changes.

## 8. References
- [NIST SP 800-175B Rev. 1](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-175B.pdf) 

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Cryptographic Control | Measures such as encryption, hashing, and digital signatures used to protect information. |
| Key Management      | The process of handling cryptographic keys

### B. Version History
Version history tracked via Git commit log.


