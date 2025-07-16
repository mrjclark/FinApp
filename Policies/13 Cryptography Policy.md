# Cryptography Policy
Document Status: Draft

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

| Role             | Responsibilities                                                                 |
|------------------|----------------------------------------------------------------------------------|
| Application Owner| Approves cryptographic methods, maintains documentation, ensures compliance.      |
| Contributors     | Adhere to cryptographic practices, report suspected weaknesses or incidents.      |

## 5. Cryptography Activities

### 5.1 Cryptographic Control Application
- Apply cryptographic controls to data at rest, in transit, and as required.

### 5.2 Algorithm and Key Management
- Use only approved algorithms, protocols, and key lengths.
- Generate, store, distribute, retire, and destroy keys securely.

### 5.3 Access and Confidentiality
- Protect private keys and passwords from unauthorized access.

### 5.4 Review and Improvement
- Regularly review cryptographic controls and update as needed.
- Implement compensating controls if encryption is not feasible.

---

## Appendix

### A. Version History
Version history is maintained in the git commit log.

### B. References
- ISO/IEC 27001:2022 Clauses A.8.24, A.10

### C. Definitions
| Word                | Definition                                                                 |
|---------------------|----------------------------------------------------------------------------|
| Cryptographic Control | Measures such as encryption, hashing, and digital signatures used to protect information. |
| Key Management      | The process of handling cryptographic keys
