---
document_ID: "S00"
title: "Standard Template"
status: "Draft"                # Options: Draft, Approved, Deprecated
document_owner: ""
document_maintainer: ""
last_approved: "YYYYMMDD"
next_review: "YYYYMMDD"
---
# Access Control Standards
Document Status: Draft  
Document Owner: mrjclark  
Document Updater: mrjclark  
Approval Date: [YYYYMMDD]  
Next Review Date: [YYYYMMDD]  

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

## 4. Implementation Guidance
TBD

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  
Cite: ISO/IEC 27001:2022, NIST SP 800-53 PM-1

## 6. Review & Maintenance
- Reviewed annually or upon significant changes.
- Change log maintained in version history or Git.

## 7. References
- ISO/IEC 27001:2022 5.15, 5.16, 5.17  
- NIST SP 800-53, 800-207  

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Termination | A contributor, whether willfully or forecully, is being removed from the project |
| Role change | A contributor who holds a currently role, is switching to a new role within the project. |

### B. Version History
Version history tracked via Git commit log.
