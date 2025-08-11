---
policy_ID: "P10"
title: "Access Control Policy"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# Access Control Policy

## 1. Purpose & Scope

### 1.1 Purpose
To define principles and requirements for managing access to information assets and resources within the FinApp project, ensuring only authorized individuals have appropriate access primarily in accordance with NIST SP 800-53 Rev. 5, and supplementarily with NIST SP 800-210.

### 1.2 Scope
This policy applies to all users, systems, applications, and resources that store, process, or transmit information within the FinApp project. All project roles are covered.

## 2. Policy Statement
The FinApp project is committed to protecting information from unauthorized access, disclosure, alteration, or destruction by enforcing strict access control measures.

## 3. Policy Objectives
- Grant access based on least privilege and business need.
- Review and adjust user access rights regularly.
- Ensure access rights are formally approved, documented, and assigned via unique user IDs.
- Control, monitor, and review privileged access.
- Avoid shared accounts; strictly control and justify if used.
- Log and monitor access to sensitive data and critical systems.
- Enforce strong authentication mechanisms.
- Secure remote access using approved methods.

## 4. Roles & Responsibilities

| Roles                     | Responsibilities                                                                 |
|---------------------------|------------------------------------------------------------------------------------|
| Senior Leadership         | - Establish access control policy, allocate resources, and ensure strategic alignment with risk posture |
| System Owner              | - Define access requirements for systems<br> - approve access authorizations and role assignments |
| Access Control Administrator | - Manage user accounts, permissions, and access provisioning<br> - enforce least privilege and separation of duties |
| Information Owner / Steward | - Classify data sensitivity<br> - define access levels and approve access to protected resources |
| Security Officer          | - Monitor access control effectiveness<br> - ensure compliance with access policies and audit requirements |
| Privacy Officer           | - Ensure access to PII is limited to authorized personnel<br> - support privacy-aware access decisions |
| IT Administrator          | - Implement technical access controls (e.g., firewalls, IAM systems)<br> - enforce session and device policies |
| Audit and Compliance Officer | - Review access logs, validate policy adherence, and report anomalies or violations |
| Identity and Access Management (IAM) Engineer | - Design and maintain authentication and authorization mechanisms<br> - support role-based and attribute-based access models |
| Application Owner         | - Define access roles and permissions for application users<br> - coordinate with system and data owners |
| Contributor / End User    | - Follow access control procedures<br> - report unauthorized access or anomalies |


## 5. Access Control Activities

### 5.1 Foundational Activities
- Develop and maintain an Access Control Policy
  - Define scope, purpose, roles, and responsibilities
  - Align with organizational risk tolerance and mission needs
- Establish procedures to implement the policy
  - Include onboarding, role assignment, access provisioning, and deprovisioning
  - Address emergency access and privileged access workflows

### 5.2 Governance and Oversight
- Review and update the policy periodically
  - At least annually or when significant system changes occur
- Ensure policy compliance across systems and users
  - Use automated tools where possible for monitoring and enforcement
- Integrate with other governance policies
  - Identity management, incident response, audit logging, and privacy

### 5.3 Control Alignment
- Support least privilege 
  - Ensure users only have access necessary for their roles
- Enforce separation of duties 
  - Prevent conflict of interest and reduce risk of fraud or error
- Define account management lifecycle 
  - Include creation, modification, disabling, and removal of accounts
- Specify access approval and revocation processes
  - Ensure timely authorization and removal of access

### 5.4 Cloud Policy Design Considerations
- Define access control models appropriate to cloud service layers
  - RBAC for IaaS and PaaS
  - ABAC for SaaS and federated identity environments
- Specify policy rules for cloud-specific access scenarios
  - Tenant isolation, cross-domain access, delegated administration

### 5.5 Cloud Policy Enforcement Mechanisms
- Ensure policy enforcement across distributed components
  - Use identity federation, token validation, centralized policy engines
- Support dynamic access decisions
  - Based on attributes like user role, device posture, location, and time

### 5.6 Governance in Cloud Context
- Map access control policies to cloud service contracts and SLAs
  - Ensure alignment with provider capabilities and organizational needs
- Document shared responsibility models
  - Clarify access control responsibilities between cloud provider and customer

## 6. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 7. Review & Maintenance
* Reviewed annually or upon significant changes.

## 8. References
- [NIST SP 800-53 Rev. 5](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf)
- [NIST SP 800-210](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-210.pdf)

---

## Appendix

### A. Definitions
| Term                | Definition                                                                 |
|---------------------|----------------------------------------------------------------------------|
| Least Privilege     | Granting users only the access necessary for their role.                   |
| Privileged Account  | Accounts with elevated access rights (e.g., administrator, root).          |
| Multi-factor Authentication | Authentication using two or more verification methods.               |

### B. Version History
Version history tracked via Git commit log.


