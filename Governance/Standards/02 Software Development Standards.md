---
document_ID: "S02"
title: "Software Development Standards"
status: "Approved"                # Options: "Draft", Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250903"
next_review: "20260903"
---
# Software Development Standards

## 1. Purpose & Scope

### 1.1 Purpose
This document is to set the minimum required precautions to be taken to ensure that development of the software is done to ensure the confidentiality and integrity of the project goals.

### 1.2 Scope
These standards apply to all systems, applications, and personnel handling or accessing sensitive data within the organization.

## 2. Roles & Responsibilities
| Role | Responsibilities |
| --- | --- |
| Owner (Project Lead) | Responsible for establishing standards, enforcing compliance, approving exceptions, and documenting exceptions with their compensating controls |
| Contributors | Responsible for tasks as given by the project lead. Reports to the project lead or documented delegate. |

## 3. Secure Development Standards

### 3.1 Software Development Process Requirements

#### 3.1.1 Concept & Initiation
- Define stakeholder protection needs and ethical boundaries.
- Identify mission/business objectives and critical assets.
- Identify high-level threats, adversaries, and potential impacts.
- Establish initial risk tolerance and trustworthiness goals.
- Document assumptions, constraints, and dependencies relevant to security.
- Identify potential loss scenarios and unacceptable consequences.
- Frame the product’s purpose as a service to others, not just a technical artifact.

#### 3.1.2 Requirements Definition
- Specify security and privacy requirements, both functional and non-functional.
- Create cyber resiliency objectives for anticipating, withstanding, recovering, and adapting.
- Align requirements with mission assurance and ethical commitments.
- Document all assumptions, constraints, and trade-offs transparently.
- Identify applicable laws, regulations, and standards.
- Perform initial risk assessment and tolerance analysis.
- Establish requirements for monitoring, detection, and response capabilities.
- Document requirements for supply chain and third-party components.

#### 3.1.3 Architecture & Design
- Apply secure design principles of least privilege, separation of concerns, defense-in-depth, and redundancy.
- Identify encryption standards for data at rest, in transit, and in use.
- Incorporate Secure by Design and Default principles.
- Perform detailed threat modeling and resilience analysis.
- Define system boundaries, trust zones, and defensive layering.
- Architect for modularity to mitigate degradation and support recovery under stress.
- Define security controls, countermeasures, and trust boundaries.
- Plan for adaptability, recovery, and continuity.
- Specify requirements for secure configuration and hardening.
- Design for secure integration with external systems and services.

#### 3.1.4 Implementation
- Enforce secure coding standards and review rituals.
- Validate and manage third-party components and SBOMs.
- Use version control, code signing, and reproducible build processes.
- Apply secure coding standards and guidelines.
- Integrate security controls into code and system components.
- Document security-relevant implementation decisions.
- Ensure traceability from requirements to implementation.
- Treat each commit as a reflection of integrity, discipline, and intentionality.

#### 3.1.5 Integration & Verification
- Conduct code and environment vulnerability assessments.
- Verify fulfillment of security and cyber resilience requirements.
- Conduct dynamic and static security testing (e.g., SAST, DAST).
- Perform penetration testing.
- Validate that security and resiliency requirements are met.
- Test system recovery, failover, and continuity mechanisms.
- Verify secure integration of third-party and supply chain components.
- Document test results and remediation actions.
- Maintain and validate assurance cases to demonstrate fulfillment of stakeholder protection needs and trustworthiness goals.

#### 3.1.6 Deployments & Operations
- Harden configurations and enforce secure defaults prior to deployment.
- Monitor for security events, anomalies, and indicators of compromise.
- Protect development and release environments with least privilege and isolation.
- Manage credentials, secrets, and access controls securely.
- Apply patches and updates in a timely manner.
- Maintain operational resilience and incident response plans.
- Conduct regular security reviews and audits of deployed systems.
- Treat operations vigilance as a practice of stewardship.
- Sustain assurance cases and traceability artifacts to support long-term trustworthiness.

#### 3.1.7 Maintenance & Disposals
- Continuously monitor for new threats and vulnerabilities.
- Patch and update software and components as needed.
- Retire or decommission components securely, ensuring data sanitization.
- Update documentation, threat models, and risk assessments.
- Review and improve security controls based on lessons learned.
- Ensure secure transfer or destruction of sensitive data and assets.
- Maintain documentation and assurance cases.
- Intentionally reflect on lessons learned and refine processes.


### 3.2 Supply Chain Management
- SecOps contributors will established a process to ensure that all third party assets (TPA) are controlled. Any vulnerabilities that are inherent in the TPA will be identified. Controls will be put into place to ensure that risks due to TPAs are reduced.
- All TPAs will require to undergo a vetting process before implementation to ensure that the security and privacy needs of the project are met. Origin, integrity, and supplier claims must be tested and confirmed. 
- FinApp design must tolerate any supplier failure or compromise.
- Every release must include a validated SBOM. Any vulnerabilities arising from TPAs must be tracked and remediated within one (1) week. Affected releases will be pulled if any vulnerabilities from TPAs that are known to be exploited outside of research.

### 3.3 Developer Access Control Management
All access control as per the S01 Access Control Implementation Standards.md are still applicable. If excess, the following access standards are implemented to any individual who will have access to development environments.
- Developers will have specific access to view, modify, and remove portions of the code base and workflows related to their code in non-production environments and branches. 
- Access to specific files will be role based. 
- No other role will have direct access to code base.
- Role authorization will be granted by a Development Lead or Project Lead. Access control decisions must be documented and traceable to role based authorization policies.
- Developers will not have access to modify access levels of their own or other roles, project security objects, or governance.
- Developers will not have access to modify or remove code or workflows from the production environment or branch.
- Developer commits will need to be verified.
- Developer access will be removed per Human Resources Standards.

### 3.4 Securing Sensitive Data
Data classified as sensitive as per the SXX Data Classification Standards.md will have the following additional standards applied:
- All sensitive data transference within FinApp will be logged in an auditable, immutable, local and centralized area.
- All sensitive data will have cryptographic measures applied when leaving the bounds of FinApp.
- All data flows will be explicitly authorized and constrained by design. This will be done by identifying trust zone, establishing flow control designs between zones, and require boundary enforcement mechanisms.
- Regular scanning for API keys, authorization token, environment secrets, and project contributor PII will be performed. Upon detection, the Project Lead and DevSecOps Lead will be notified. Any releases containing this information will be pulled until all information leakage has been handled.
- Sensitive data flows must be documented in data flow diagrams and reviewed annually, or upon data flow changes.

### 3.5 Contributor Verifications
In the event that the FinApp project team exceeds ten (10) people, or should the FinApp project be reorganized to handle sensitive data, the following Contributor Verification program will be activated that will contain the following minimum standards:
- A segregation of duty review will be performed to separate privileged accesses from being able to develop and deploy code
- A review of all roles will be done to ensure that there is the least privileges needed to perform the duties
- Auditing procedures will be reviewed to ensure that it can identify contributor actions
- A senior contributor will be elected as the Responsible Steward to oversee monitoring. The Responsible Steward must maintain a log of privileged actions and review anomolies monthly.
- Scrutiny will be placed on actions that are deemed to misuse privileged access, bypass established controls, undermine project confidentiality and integrity goals, and cause any discord in project operations or team collaboration.

### 3.6 System Exposure Considerations
- All system boundaries must be documented in system diagrams and reviewed annually, or upon relevant subsystem changes.
- All communication within the project team will occur over approved channels
- FinApp subsystems will be separated from each other through logical divisions
- The code base will be regularly and automatically scanned for vulnerabilities that may expose the system to degradation of the FinApp's confidentiality or integrity. Any scans that successfully find a vulnerability must be acknowledged and action must be taken to handle the vulnerability.
- To the extent possible, review port and repository scans that are coming from unfamiliar locations. Persistent, unknown activity is to be blocked from the project.
- The code base will be regularly and automatically scanned for vulnerabilities that may expose the system to degradation of the FinApp's confidentiality or integrity.
- A complete and accurate list of the system inventory, including TPAs, project developed code, documentation, workflows, and security architecture will be kept and updated regularly, or upon change. If a system inventory reconciliation shows unaccounted for items, a review of the new items will take place to determine the origin, risk, and removal of the item. If the item is from an unknown origin, a change of environment secrets, API keys, access keys and signing will be completed where necessary.

### 3.5 Incident Handling with New Vulnerabilities
- Any recently reported vulnerabilities will be identified, logged, and a plan for correction will be determined.
- Any releases containing a vulnerability will be tagged and communicated to all stakeholders.
- Remediation of the flaw documented along with any potential side effects.
- Remediations will be incorporated into automatic testing and release deployment.

### 3.6 General Coding Standards
- All coding standards from the [OWASP Secure Coding](https://owasp.org/www-project-secure-coding-practices-quick-reference-guide/stable-en/02-checklist/05-checklist) Practices will be upheld.
- All contributors must complete secure coding checks as part of all pull requests.

## 4. Implementation Guidance

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  

## 6. Review & Maintenance
 Reviewed annually or upon significant changes.

## 7. References
- NIST SP 800-53 Rev 5, 800-218 Ver 1.1, 800-160 Vol 1 Rev 1
- OWASP Secure Coding Practices
- Internal policy or repo links (if applicable)
- [S03 Data Classification Standard.md](./"S03 Data Classification Standard.md)

## 8. Audit & Traceability
- Compliance is verified through quarterly reviews of implementation artifacts.
- Contributors will be asked to attest to adherence via signed commits or onboarding checklists.

---

## Appendix

### A. Definitions
## Appendix A: Terms and Definitions

| Term                  | Definition                                                                 |
|-----------------------|----------------------------------------------------------------------------|
| TPA (Third Party Asset) | Any external software, library, or service integrated into FinApp systems. Must be vetted for origin, integrity, and licensing. |
| SBOM (Software Bill of Materials) | A formal record of all components, libraries, and dependencies used in a software system. Enables supply chain transparency and vulnerability tracking. |
| Trust Zone        | A logically separated environment with defined access controls and data sensitivity boundaries. Used to isolate critical assets and reduce attack surface. |
| Responsible Steward | A designated contributor accountable for verifying standards adherence, reviewing privileged actions, and maintaining audit logs. |
| Secure Coding Checklist | A contributor-facing list of secure development practices aligned with OWASP and SSDF, used to validate commits and onboarding readiness. |
| Privileged Action | Any operation that modifies system configuration, accesses sensitive data, or alters access controls. Must be logged and reviewed. |
| Audit Artifact    | Any document, log, diagram, or checklist that provides evidence of standards adherence and operational integrity. |
| Remediation Plan  | A structured response to identified vulnerabilities or incidents, including root cause analysis, corrective actions, and regression testing. |

### B. Version History
Version history tracked via Git commit log.
