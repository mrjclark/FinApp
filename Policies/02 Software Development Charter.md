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

### 2.1 Secure Software Development Processes
| Process | Key Activities | Purpose |
| --- | --- | --- |
| Concept and Initiation | Define stakeholder protection needs; Identify security objectives and contraints; and establish trustworthiness goals | Ground the project in intentional security from the beginning |
| Requirements Definition | Specify security requirements, both functional and non-functional; Include risk identification and tolerance; Align with protection needs | Ensure security is implemented into security expectations | 
| Archtecture & Design | Apply security design principles; Perform threat modeling; Define seucirty interfaces and boundaries | Build resilience in the project's structure |
| Implementation | Ensure secure coding standards; Validate 3rd party components; User version control and code signing | Translate design into trustworth code |
| Integration & Verification | Conduct code analysis; Perform security testing; Validate security requirements are met | Confirm the system behaves securely under scrutiny |
| Deployments & Operations | Harden configurations; Monitor for anomolies; Protect released product environment | Maintain security posture in post release |
| Maintenance & Disposals | Patch vulnerabilities; Retire components securely; Update threat models and documentation | Sustain trustworthiness over time |


### 2.3 Secure Architecture & Design
- Follow a zero-trust model for authentication and access controls.
- Implement encryption standards (AES for data at rest, TLS for data in transit).
- Reduce attack surfaces using least privilege access control.
- Development should always include principles of Secure by Design and Default
- 

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