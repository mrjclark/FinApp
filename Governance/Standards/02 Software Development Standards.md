---
document_ID: "S00"
title: "Standard Template"
status: "Draft"                # Options: Draft, Approved, Deprecated
document_owner: ""
document_maintainer: ""
last_approved: "YYYYMMDD"
next_review: "YYYYMMDD"
---
# Information Security Standards
Document Status: Draft
Document Owner: mrjclark
Document Updater: mrjclark
Approval Date:  
Next Review Date:

## 1. Purpose & Scope

### 1.1 Purpose
This standard defines the minimum security requirements for access control, authentication, and encryption to protect sensitive information within the organization’s systems and data.

### 1.2 Scope
These standards apply to all systems, applications, and personnel handling or accessing sensitive data within the organization.

## 2. Roles & Responsibilities
| Role | Responsibilities |
| --- | --- |
| Owner (Project Lead) | Responsible for establishing standards, enforcing compliance, approving exceptions, and documenting exceptions with their compensating controls |
| Contributors | Responsible for tasks as given by the project lead. Reports to the project lead or documented delegate. |

## 3. Access Control Implementation

### 3.1 Principle of Least Privilege
- Users, processes, and devices shall be granted the minimum access necessary to perform their job functions.
- Access reviews must be conducted at least yearly, and after any significant change in role, project, or system (ISO/IEC 27001:2022, NIST SP 800-53 AC-6).

### 3.2 Role-Based Access Control (RBAC)
- Define and maintain roles with specific permissions.
- Assign users to roles based on job responsibilities.
- Document all roles and associated permissions.
- Review and update roles and permissions at least annually, or after significant organizational changes (ISO/IEC 27001:2022, NIST SP 800-53 AC-2).

### 3.3 Access Requests and Approvals
- All access requests must be formally submitted and approved by the project owner.
- Maintain records of all access requests, approvals, and removals.
- Implement automated workflows for access provisioning and de-provisioning where feasible (ISO/IEC 27005, NIST SP 800-53 AC-2, 800-207 Zero Trust).

### 3.4 Access Revocation
- Access must be immediately revoked upon termination or role change.
- Automated processes for account de-provisioning must be implemented.
- Conduct quarterly audits to verify timely removal of access (ISO/IEC 27001:2022, NIST SP 800-53 AC-2).

## 4. Secure Authentication Requirements

### 4.1 Multi-Factor Authentication (MFA)
- MFA must be enabled for all privileged and remote access accounts.
- At least two factors (something you know, have, or are) must be used.
- MFA mechanisms must be reviewed annually for effectiveness and compliance (ISO/IEC 27001:2022, NIST SP 800-53 IA-2, 800-207).

### 4.2 User Password Policy
- Minimum password length: 12 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 5 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).
- Password changes required at least every 180 days, or immediately after suspected compromise (ISO/IEC 27001:2022, NIST SP 800-53 IA-5).

### 4.3 Privileged User Password Policy
- Privileged accounts are defined as those which have direct access to change source code in the project.
- Minimum password length: 24 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 10 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).
- Privileged account passwords must be changed at least every 90 days (ISO/IEC 27001:2022, NIST SP 800-53 IA-5).

### 4.4 System Account Password Policy
- System accounts are used for system to system communication only.
- System accounts shall not be used to interactively access project resources through human operation.
- Minimum password length: 24 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 10 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).
- System account credentials must be rotated at least every 180 days (ISO/IEC 27001:2022, NIST SP 800-53 IA-5).

### 4.5 Session Management
- Invalidate sessions after password changes or account lockout.
- Sessions must timeout after 15 minutes of inactivity (ISO/IEC 27001:2022, NIST SP 800-53 AC-12).

### 4.6 Account Lockout
- Lock accounts after 10 failed login attempts within 10 minutes.
- Locked accounts can be unlocked only by an administrator or through secure self-service.
- Log all lockout events and review for signs of brute force attacks (ISO/IEC 27001:2022, NIST SP 800-53 AC-7).

## 5. Encryption Standards

### 5.1 Data at Rest
- All sensitive data must be encrypted at rest using industry-standard algorithms (e.g., AES-256).
- Encryption keys must be managed securely, with access restricted to authorized personnel only.
- Regularly rotate encryption keys and audit key usage.
- Document key management procedures and review annually (ISO/IEC 27001:2022, 27017, 27018, NIST SP 800-53 SC-13, 800-57).

### 5.2 Data in Transit
- All data transmitted over public or untrusted networks must use TLS 1.2 or higher.
- Disable insecure protocols (e.g., SSL, TLS 1.0/1.1).
- Validate certificates and reject expired or self-signed certificates in production systems.
- Document and review encryption protocols annually (ISO/IEC 27001:2022, NIST SP 800-53 SC-8, 800-52).

### 5.3 Data in Use
- All data viewed or processed will be subject to role-specific access.
- Data for viewing or processing will be removed when no longer needed or after a 10 minute inactivity period.
- Changes to data shall be logged

## 6. Compliance and Monitoring
- Quarterly audit access control, authentication, and encryption configurations.
- Document and remediate any deviations from these standards.
- Provide training to ensure personnel understand and follow these requirements.
- Maintain audit logs for at least 1 year and review monthly for suspicious activity (ISO/IEC 27001:2022, 27701, NIST SP 800-53 AU-6).

## 7. Secure Coding

## 8. Code Quality

## 9. Version Control

## 10. Secure Build & CI/CD

## 11. Testing Standards

## 12. Documentation


## 10. Change Management
- Document and approve all changes to systems, applications, and infrastructure.
- Assess security impact of changes before implementation.
- Maintain records of all changes and associated approvals.
- Review change management process annually (ISO/IEC 27001:2022, NIST SP 800-53 CM-3).

## 14. Release Management


## 11. Vulnerability Management
- Regularly scan systems and applications for vulnerabilities.
- Prioritize and remediate vulnerabilities based on risk.
- Track and document remediation efforts.
- Conduct vulnerability assessments at least quarterly (ISO/IEC 27001:2022, NIST SP 800-53 RA-5).

## 12. Security Awareness and Training
- Provide regular security awareness training to all personnel.
- Ensure training covers secure development practices, data protection, and incident reporting.
- Document attendance and completion of training (ISO/IEC 27001:2022, 27701, NIST SP 800-53 AT-2).

## 14. Implementation Guidance
Any supporting documentation on implementation requirements is listed here

## 16. Exceptions
Any exceptions to this standard must be formally documented, risk-assessed, and approved by the Information Security Officer. Exceptions must be reviewed at least annually (ISO/IEC 27001:2022, NIST SP 800-53 PM-1).

## 17. Review
This standard shall be reviewed at least annually or upon significant changes to relevant technology or regulations.

---

## Appendix

### A. Version History
Version history is maintained in the git commit log.

### B. References
- ISO/IEC 27001:2022 (Information Security Management Systems)
- ISO/IEC 27002:2022 (ISMS Implementation Guidance)
- ISO/IEC 27005 (Information Security Risk Management)
- ISO/IEC 27017 (Cloud Security Controls)
- ISO/IEC 27018 (Protection of PII in Public Clouds)
- ISO/IEC 27036 (Supplier Relationships)
- ISO/IEC 27701 (Privacy Information Management)
- ISO/IEC 22301 (Business Continuity Management)
- NIST SP 800-53 Rev 5 (Security and Privacy Controls)
- NIST SP 800-160 Vol 1 & 2 (Systems Security Engineering)
- NIST SP 800-218 v1.1 (Secure Software Development Framework)
- NIST SP 800-207 (Zero Trust Architecture)
- NIST SP 800-61 (Incident Response)
- NIST SP 800-57 (Key Management)
- NIST SP 800-52 (TLS Guidelines)

### C. Definitions
| Word                | Definition                                                                 |
|---------------------|----------------------------------------------------------------------------|
| Principle of Least Privilege | Granting users, processes, and devices only the access necessary for their roles. |
| Role-Based Access Control (RBAC) | Access control method assigning permissions to roles rather than individuals. |
| Multi-Factor Authentication (MFA) | Authentication using two or more verification methods (factors). |
| Privileged Account  | Account with elevated access rights, such as administrator or root.         |
| System Account      | Account used for system-to-system communication, not for human access.      |
| Data at Rest        | Data stored on disk or other persistent media.                              |
| Data in Transit     | Data actively moving across networks.                                       |
| SSDLC               | Secure Software Development Lifecycle: integrating security into all phases of software development. |
| Vulnerability Assessment | Process of identifying, quantifying, and prioritizing vulnerabilities in a system. |
| Incident Response   | Organized approach to addressing and managing the aftermath of a security breach or attack. |
| Audit Log           | Record of events and changes in a system for monitoring and forensic analysis. |



