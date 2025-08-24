---
document_ID: "S01"
title: "Access Control Implementation Standards"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250811"
next_review: "20260811"
---
# Access Control Implementation Standards

## 1. Purpose & Scope

### 1.1 Purpose
This standard defines the minimum security requirements for access control to protect sensitive information within the organization’s systems and data.

### 1.2 Scope
These standards apply to all systems, applications, and personnel handling or accessing sensitive data within the organization.

## 2. Roles & Responsibilities
| Role | Responsibilities |
| --- | --- |
| Owner (Project Lead) | Responsible for establishing standards, enforcing compliance, approving exceptions, and documenting exceptions with their compensating controls |
| Contributors | Responsible for tasks as given by the project lead. Reports to the project lead or documented delegate. |
| Access Control Steward | - Maintain access control policies and procedures<br>- Ensure alignment with NIST SP 800-53 and SP 800-207<br>- Oversee periodic reviews and updates |
| System Owner | - Define access requirements for systems<br>- Approve role definitions and access levels<br>- Participate in access reviews |
| Information System Security Officer (ISSO) | - Monitor access control compliance<br>- Investigate anomalies and violations<br>- Coordinate with audit and incident response teams |
| Identity & Access Management (IAM) Administrator | - Provision and de-provision user accounts<br>- Implement RBAC and least privilege<br>- Maintain access logs and audit trails |
| Audit & Compliance Lead | - Conduct periodic access reviews and audits<br>- Validate control effectiveness<br>- Report findings to governance bodies |
| Contributor / End User | - Request access through approved workflows<br>- Use credentials responsibly<br>- Report access issues or anomalies |
| Zero Trust Architect / Engineer | - Design and maintain policy enforcement points (PEPs)<br>- Integrate contextual signals into access decisions<br>- Ensure continuous authentication and authorization |
| HR / People Operations | - Notify IAM team of role changes, terminations, or onboarding<br>- Support separation of duties and least privilege enforcement |


## 3. Access Control Implementation

### 3.1 Principle of Least Privilege
- Users, processes, and devices shall be granted the minimum access necessary to perform their job functions.
- Access reviews must be conducted at least yearly, and after any significant change in role, project, or system.

### 3.2 Role-Based Access Control (RBAC)
- Define and maintain roles with specific permissions.
- Assign users to roles based on job responsibilities.
- Document all roles and associated permissions.
- Review and update roles and permissions at least annually, or after significant organizational changes.

### 3.3 Access Requests and Approvals
- All access requests must be formally submitted and approved by the project owner.
- Maintain records of all access requests, approvals, and removals.
- Implement automated workflows for access provisioning and de-provisioning where feasible.

### 3.4 Access Revocation
- Access must be immediately revoked upon termination or role change.
- Automated processes for account de-provisioning must be implemented.
- Conduct quarterly audits to verify timely removal of access.

### 3.5 Access Logging & Monitoring
- All access events must be logged and retained for at least 12 months.
- Logs must include user ID, timestamp, resource accessed, and action taken.
- Implement automated alerts for anomalous access patterns.

### 3.6 Zero Trust Architecture Alignment
- Access decisions must be dynamic and context-aware.
- Implement policy enforcement points (PEPs) that evaluate identity, device posture, and behavior.
- Require continuous authentication and authorization for sensitive resources.

### 3.7 User Password Policy
- Minimum password length: 12 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 5 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).
- Password changes required at least every 180 days, or immediately after suspected compromise (ISO/IEC 27001:2022, NIST SP 800-53 IA-5).

### 3.8 Privileged User Password Policy
- Privileged accounts are defined as those which have direct access to change source code in the project.
- Minimum password length: 24 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 10 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).
- Privileged account passwords must be changed at least every 90 days (ISO/IEC 27001:2022, NIST SP 800-53 IA-5).

### 3.9 System Account Password Policy
- System accounts are used for system to system communication only.
- System accounts shall not be used to interactively access project resources through human operation.
- Minimum password length: 24 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 10 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).
- System account credentials must be rotated at least every 180 days (ISO/IEC 27001:2022, NIST SP 800-53 IA-5).

### 3.10 Session Management
- Invalidate sessions after password changes or account lockout.
- Sessions must timeout after 15 minutes of inactivity (ISO/IEC 27001:2022, NIST SP 800-53 AC-12).

### 3.11 Account Lockout
- Lock accounts after 10 failed login attempts within 10 minutes.
- Locked accounts can be unlocked only by an administrator or through secure self-service.
- Log all lockout events and review for signs of brute force attacks (ISO/IEC 27001:2022, NIST SP 800-53 AC-7).

## 4. Implementation Guidance
TBD - procedures to be added

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  

## 6. Review & Maintenance
- Reviewed annually or upon significant changes.
- Change log maintained in version history or Git.

## 7. References 
- NIST SP 800-53 Rev. 5
- NIST SP 800-207

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Termination | A contributor, whether willfully or forecully, is being removed from the project |
| Role change | A contributor who holds a currently role, is switching to a new role within the project. |
| Access Control | The process of granting or denying specific requests to obtain and use information and related services. |
| Least Privilege | The principle that users and systems should only have the minimum level of access necessary to perform their duties. |
| Role-Based Access Control (RBAC) | A method of regulating access based on the roles of individual users within an organization. |
| Access Review | A periodic evaluation of user access rights to ensure they are appropriate and aligned with current responsibilities. |
| De-provisioning | The process of removing access rights or disabling accounts when users leave or change roles. |
| Policy Enforcement Point (PEP) | A system component that enforces access decisions based on policy, identity, and context. |
| Zero Trust Architecture (ZTA) | A security model that assumes no implicit trust and requires continuous verification of identity and context before granting access. |
| Identity Provider (IdP) | A system that authenticates users and provides identity information to relying systems. |
| Contextual Access | Access decisions that consider additional factors such as device health, location, time, and behavior. |
| Audit Trail | A chronological record of system activities that is used to detect and investigate security incidents. |
| Exception | A documented deviation from the standard, approved through a formal risk assessment and review process. |
| Termination | A contributor, whether willfully or forcefully, is being removed from the project. |
| Role Change | A contributor who holds a current role is switching to a new role within the project. |

### B. Version History
Version history tracked via Git commit log.
