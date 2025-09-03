---
standard_ID: "S04"
title: "Audit Standards"
status: "Approved"       # Options: "Draft", "Approved", "Deprecated"  
document_owner: "mrjclark"  
document_maintainer: "mrjclark"  
last_approval: "20250903"  
next_review: "20260903"  
---

# Audit Standards

## 1. Purpose & Scope

### 1.1 Purpose
This will define the minimum requirements for auditing in FinApp so that there is an immutable and informative source of information to be reviewed when required to understand the order of events in either the development or internal workings of the application. 

### 1.2 Scope
This document applies to all development, repositories, FinApp assets, and contributors in the project. 

## 2. Roles & Responsibilities
List key roles and what they’re expected to do.
| Role | Responsibilities |
|------|------------------|
| Audit Lead | Reviews audit incident reports and creates updated security requirements. |
| Auditor | Establishes and enforces the standard. Reviews and approves exceptions. |
| DevSecOps Lead | Reviews security requirements gathered from audit reviews and does necessary risk assessment. |
| DevSecOps | Implements security requirements for audit logs and reviews audit logging failures. |
| Incident Handler | Analyze created issues, gathers additional required information, and assigns tasks to the appropriate group |
| User | Approves requests to send audit failure logs, or archive, move, and delete audit logs |

## 3. Standard Requirements

### 3.1 Auditable Events & Contents
- Event types include password changes, failed logons or failed accesses related to systems, security or privacy attribute changes, administrative privilege usage, PIV credential usage, data action changes, query parameters, or external credential usage
- Auditable events must be logged with what type of event occurred, when it occurred, the location or system where the event occurred, the immediate source of where the event came from, the outcome of the event, and the identity of the system or user at the source that initiated the event.
- Audit logs must not contain PFI.
- Audit logs must contain non-repudiable evidence of the identity of the system or user that initiated an event.
- Audit event logging must be done consistently across the entire scope
- Audit event logging must be automated

### 3.2 Audit Log Immutability and Security
- Access to review audit logs must only be given to users with the Auditor role
- System processes must log all auditable events to audit logs, but must not view, modify or delete any portion or whole log
- The ability to archive or remove audit logs must only be given to administrative audit system processes when retention requirements are met, or with authorized permission
- Audit logs must be stored so that a 4-eyes approval is required before being modified or deleted
- If an administrative process or privileged user attempts to override the 4-eyes approval, an attempt to backup and off-load the affected log must be made 
- All audit logs from the user environment must be combined and stored centrally
- Audit logs must be made available upon demand and searchable using any attribute within the log
- Audit logs must be uniquely encrypted as per SXX Cryptography Standards.md s o only authorized processes are able to read them

### 3.3 Failures During Audit Event Logging
- When an audit event cannot be logged in the development environment, the DevSecOps roles must be notified immediately
- When an audit event cannot be logged in the user environment, an option to notify the DevSecOps must be given at least twice
- When the storage system containing the logs is at 90% or higher, a notification must be sent to acknowledge. In the development environment, the notification must be sent to the DevOps group. In the user environment, the notification must be sent to the user.
- Audit event logging failures in the user environment must trigger an attempt to write the event to one a separate location.

### 3.4 Audit Log Review Triggers & Actions
- An incident must be logged as described in SXX Incident Handling Standards.md when: 
    - An audit event logging failure occurs by someone with the DevSecOps roles
    - An audit log shows successful or unsuccessful unauthorized access attempts of 5 times or more by the same identity to the same target within any 24 hour time frame
    - An audit log is not able to obtain non-repudiation of an access attempt to audit logs
- When an incident is created, an user with the Incident Response role must assign to Auditors to review
- A user with the Auditor role must create a suggested response for an Audit Lead to approve.
- The Audit Lead must give updated security requirements to the DevSecOps Lead for risk assessment as per SXX Risk Assessment Standards.md 

### 3.5 Audit Log Retention
- Commit audit logs must be kept indefinitely
- Release build logs in a production environment must be kept for 3 years after the end of life of the release
- Release build logs in a non-production environment must be kept for 1 week
- Audit logs and security scan logs in the development environment must be kept for 1 year
- In the event that storage space must be made, audit logs must be archived and moved to a new location. In the development environment, an incident must be logged as per SXX Incident Handling Standards.md. In the user environment, the user must be given the choice to archive and move, or archive and delete the audit log

## 4. Implementation Guidance

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  

## 6. Review & Maintenance
- Reviewed annually or upon significant changes.

## 7. References
- NIST SP 800-53 Rev. 5
- SXX Incident Handling Standards.md
- SXX Risk Assessment Standards.md

## 8. Audit & Traceability
- Compliance is verified through periodic reviews of implementation artifacts.
- Contributors may be asked to attest to adherence via signed commits or onboarding checklists.

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Audit Event | A recorded occurrence of a system or user action that is relevant to security, privacy, or operational integrity. |
| Audit Log | A chronological record of audit events, including metadata such as timestamp, source, outcome, and identity. |
| PIV Credential | A Personal Identity Verification credential issued under FIPS 201 for secure authentication and access control. |
| 4-Eyes Approval | A dual-authorization mechanism requiring two distinct individuals to approve a sensitive action before execution. |
| Non-Repudiation | Assurance that the origin and integrity of an audit event cannot be denied or altered. |
| Immutable Log | A log structure that cannot be modified or deleted once written, enforced through cryptographic or system-level controls. |
| Audit Lead | A designated role responsible for interpreting audit findings and updating security requirements. |
| Audit Trail | A complete and verifiable sequence of audit events that supports forensic analysis and accountability. |
| Tamper Detection | Mechanisms that identify unauthorized changes to audit logs or audit-related processes. |

### B. Version History
Version history tracked via Git commit log.
