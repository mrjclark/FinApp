---
policy_ID: "P02"
title: "Software Development Charter"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# Software Development Charter

## 1. Purpose & Scope

### 1.1 Purpose
This charter, endorsed by project leadership, is grounded in the principles of systems security engineering as defined in NIST SP 800-160 Vol. 1 Rev. 1, "Engineering Trustworthy Secure Systems." It emphasizes stakeholder protection needs, mission assurance, and cyber resiliency across the system life cycle.

### 1.2 Scope
- Applies to all phases of development, as well as all assets created as part of the development.
- Covers the development process, risk management, and secure coding practices.

## 2. Policy statement
FinApp is committed to using secure development practices to ensure data confidentiality and integrity using industry standards. The development will be transparent and process driven to ensure trustworthiness and accountbility.

## 3. Secure Software Development Life Cycle
- The development of FinApp will occur using a set process. 
- Processes are designed to be overlapping and can contain parallel tasks and activities. 
- Tasks and activities can transfer from one process to the next if it fulfills the requirements of that process. Tasks and activities from one process can also transfer to any of the previous process when new or existing requirements were found to be missing.
- Requirements will be determined by the task or activity responsible upon creation or transfer to another process.

### 3.1 Secure Software Development Processes
| Process |  Purpose |
| --- | --- |
| Concept & Initiation |  Ground the project in intentional security from the beginning |
| Requirements Definition | Ensure security is implemented into security expectations | 
| Archtecture & Design | Build resilience in the project's structure |
| Implementation | Translate design into trustworth code |
| Integration & Verification | Confirm the system behaves securely under scrutiny |
| Deployments & Operations | Maintain security posture in post release |
| Maintenance & Disposals | Sustain trustworthiness over time |


## 4. Roles & Responsibilities
| Role                            | Responsibilities                                                                                    |
|---------------------------------|-----------------------------------------------------------------------------------------------------|
| Owner / Project Lead            | Accountable for approving and reviewing this charter and ensuring adequate resources for security.  |
| Lead Developer                  | Oversee secure development practices, architecture, and documentation.                              |
| Security Reviewer               | Perform code audits, vulnerability scans, and compliance checks; independent of implementation team.|
| Incident Response Handler       | Define and coordinate recovery strategies in case of security breaches.                             |
| Contributors/Developers         | Follow secure coding guidelines and report security concerns.                                       |
| System Administrator/DevOps     | Secure deployment environments and manage access controls.                                          |
| Data Protection Officer         | Oversee compliance with privacy regulations and data protection requirements.                       |
| Third-Party/Vendor              | Adhere to project’s security requirements when engaged.                                             |


## 5. Continuous Security Improvement Commitement
- Continuous reviews on security will be needed as per industry standards for secure software development
- Auditing will be done to ensure security controls are working as expected
- Security controls will be updated as needed when emerging risks to development materialize

## 6. Secure Coding and Review Practices
- The use of secure coding standards, regular code reviews, and automated/static analysis to detect vulnerabilities will be implemented 

## 7. Supply Chain Security
- All third-party components, libraries, and dependences will be evaluated before use and quarterly for security and compliance.

## 8. Segregation of Duties
- Where separation of duties is not feasible due to team size, compensating controls will be implemented as described in the supplemental control documentation.
- Compensating controls will be automated where possible.
- When compensating controls cannot be automated, approval of compensating controls will be given by the project lead and reviewed quarterly for necessity.

## 9. Continuous Security Training and Awareness
- All contributors will undergo security training and policy awareness during onboarding and once per calendar year.

## 10. Incident Response and Learning
- All incidents that comprimise the confidentiality, integrity or availability of the development will have a timely incident detection, response, and post-incident reviews to drive continual improvement.

## 11. Change Management and Configuration Control
- All changes to code, infrastructure, and configurations are controlled, documented, and reviewed for security impact.

## 12. Asset and Data Classification
- All data and assets will require a classification to ensure appropriate protection measures are applied.

## 13. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 14. Review & Maintenance
* Reviewed annually or upon significant changes.

## 15. References
- [NIST SP 800-160 Vol. 1 Rev. 1: Engineering Trustworthy Secure Systems](https://csrc.nist.gov/pubs/sp/800/160/v1/r1/final)
- [OWASP SAMM](https://owaspsamm.org/about/)

---

## Appendix

### A. Version history
- Version history is maintained in the Git commit log

