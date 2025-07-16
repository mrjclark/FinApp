# Software Development Charter

## 1. Purpose & Scope

### 1.1 Purpose
This charter, endorsed by project leadership, defines the security principles and commitments guiding the development of FinApp. It establishes clear roles, responsibilities, and governance for secure development using industry standards based around ISO27001:2022 and NIST SSDF 800 series.

### 1.2 Scope
- Applies to all phases of development, as well as all assets created as part of the development.
- Covers the development process, risk management, and secure coding practices.

## 3 Secure Development Framework
- Adhere to industry standards for secure software development 
- Conduct threat modeling and security assessments at all development phases.

## 2. Secure Software Development Life Cycle
- The development of FinApp will occur using the below processes. 
- Processes are designed to be overlapping and can contain parallel tasks and activities. 
- Tasks and activities can transfer from one process to the next if it fulfills the requirements of that process. Tasks and activities from one process can also transfer to any of the previous process when new or existing requirements were found to be missing.
- Requirements will be determined by the task or activity responsible upon creation or transfer to another process.

### 2.1 Secure Software Development Processes
| Process |  Purpose |
| --- | --- |
| Concept and Initiation |  Ground the project in intentional security from the beginning |
| Requirements Definition | Ensure security is implemented into security expectations | 
| Archtecture & Design | Build resilience in the project's structure |
| Implementation | Translate design into trustworth code |
| Integration & Verification | Confirm the system behaves securely under scrutiny |
| Deployments & Operations | Maintain security posture in post release |
| Maintenance & Disposals | Sustain trustworthiness over time |

### 2.2 Concept and Initiation
- Define stakeholder protection needs and ethical boundaries.
- Establish trustworthiness goals and resiliance objectives.
- Frame the final products purpose as a service to others, not just a technical artifact.
- Identify potential loss scenarios and unnacceptable consequences.

### 2.3 Requirements Definition
- Specify security and privacy requirements, both functional and non-functional.
- Create cyber resiliency objectives for anticipating, withstanding, recovering and adapting.
- Align requirements with mission assurance and ethical commitments.
- Document all assumations, contraints, and trade-offs transparently.

### 2.4 Architecture & Design
- Apply secure design principles of least privilege and separation of concern.
- Identify encryption standards for data at rest, in transit and in use.
- Development will always include principles of Secure by Design and Default.
- Perform threat modeling and resilience analysis.
- Define system boundaries, trust zones, and defensive layering.
- Architect for modularity to mitigate degradation and recovery under stress.

### 2.5 Implementation
- Enfore secure coding standards and review rituals.
- Validate third-party components and SBOM's.
- Use version control, code signing and reproducible build processes.
- Treat each commit as a reflection of integrity, discipline and intentionality.

### 2.6 Integration & Verification
- Conduct code and environment vulnerability assessments.
- Verify fulfillment of security and cyber resiliance requirements.

### 2.7 Deployments & Operations
- Harden configurations and enforce secure defaults.
- Monitor for anomalies and indicators of comprimise.
- Protect development and release environments with least privilege and isolation.
- Treat operations vigilance as a practice of stewardship.

### 2.8 Maintenance & Disposals
- Patch vulnerabilities as the need arises based on prioritization.
- Retire components securely to preserve data confidentiality.
- Maintain documentation and assurance cases.
- Intentionally reflect on lessons learned and refine processes.

## 3. Roles & Responsibilities
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



## 4. Continuous Security Improvement Commitement
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

## 13. Periodic Review and Audit
- There will be annual reviews and audits of security controls, policies, and procedures.

## 14. Policy Reference & Hierarchy
- This charter operates under the [Information Security Policy](./Information%20Security%20Policy.md) and is supported by related policies, standards, and procedures.

---

## Appendix

- References: [NIST SSDF](https://csrc.nist.gov/publications/detail/white-paper/2022/secure-software-development-framework/final), [OWASP](https://owasp.org/), ISO/IEC 27001:2022
- Version history is maintained in the Git commit log
- Status: Draft