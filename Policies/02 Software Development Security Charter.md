# Software Development Security Charter

## 1. Purpose & Scope

### 1.1 Purpose
This charter, endorsed by project leadership, defines the security principles and commitments guiding the development of FinApp. It establishes clear roles, responsibilities, and governance for secure development using industry standards based around ISO27001:2022 and NIST SSDF 800 series.

### 1.2 Scope
- Applies to all phases of development, as well as all assets created as part of the development.
- Covers the development process, risk management, and secure coding practices.

## 2. Secure Software Development Life Cycle

### 2.1 Processes

| Process | Key Activities | Purpose |
| --- | --- | --- |
| Concept and Initiation | Define stakeholder protection needs; Identify security objectives and contraints; and establish trustworthiness goals | Ground the project in intentional security from the beginning |
| Requirements Definition | Specify security requirements, both functional and non-functional; Include risk identification and tolerance; Align with protection needs | Ensure security is implemented into security expectations | 
| Archtecture & Design | Apply security design principles; Perform threat modeling; Define seucirty interfaces and boundaries | Build resilience in the project's structure |
| Implementation | Ensure secure coding standards; Validate 3rd party components; User version control and code signing | Translate design into trustworth code |
| Integration & Verification | Conduct code analysis; Perform security testing; Validate security requirements are met | Confirm the system behaves securely under scrutiny |
| Deployments & Operations | Harden configurations; Monitor for anomolies; Protect released product environment | Maintain security posture in post release |
| Maintenance & Disposals | Patch vulnerabilities; Retire components securely; Update threat models and documentation | Sustain trustworthiness over time |

### 2.2 Secure Development Framework
- Adhere to NIST SSDF V1.1 guidelines as the primary framework.
- Implement OWASP secure coding principles.
- Conduct threat modeling and security assessments at key development phases.

### 2.3 Secure Architecture & Design
- Follow a zero-trust model for authentication and access controls.
- Implement encryption standards (AES for data at rest, TLS for data in transit).
- Reduce attack surfaces using least privilege access control.

## 3. Roles & Responsibilities

| Role                           | Responsibilities                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------|
| **Project Owner/Senior Manager**| Accountable for approving and reviewing this charter and ensuring adequate resources for security.   |
| **Lead Developer**              | Oversee secure development practices, architecture, and documentation.                              |
| **Security Reviewer**           | Perform code audits, vulnerability scans, and compliance checks; independent of implementation team.|
| **Incident Response Handler**   | Define and coordinate recovery strategies in case of security breaches.                             |
| **Contributors/Developers**     | Follow secure coding guidelines and report security concerns.                                       |
| **System Administrator/DevOps** | Secure deployment environments and manage access controls.                                          |
| **Data Protection Officer**     | Oversee compliance with privacy regulations and data protection requirements.                       |
| **Third-Party/Vendor**          | Adhere to project’s security requirements when engaged.                                             |

- Segregation of Duties: Where separation of duties is not feasible due to team size, compensating automated controls are implemented as described in the supplemental control documentation.
- Security Awareness & Training: All roles must complete periodic security awareness training appropriate to their responsibilities.

## 4. Secure Development Lifecycle (SDLC)

### 4.1 Planning & Design
- Identify security risks and define mitigation strategies.
- Establish secure coding guidelines.

### 4.2 Implementation
- Enforce input validation and parameterized queries to prevent SQL injection.
- Secure API interactions with authentication and authorization.

### 4.3 Testing
- Perform static and dynamic analysis to detect vulnerabilities.
- Implement penetration testing for security validation.

### 4.4 Deployment & Maintenance
- Monitor for vulnerabilities using automated scanning tools.
- Apply patch management and updates to mitigate risks.

## 5. Compliance, Reporting & Continuous Improvement

### 5.1 Compliance Standards
- Document adherence to SSDF and ISO/IEC 27001 security requirements.
- Maintain audit logs for development activities.

### 5.2 Reporting & Escalation
- Security incidents or concerns must be reported promptly to the Project Owner or Security Reviewer for investigation and response.

### 5.3 Continuous Security Improvement
- Conduct periodic security assessments.
- Update security policies based on emerging threats.

## 6. Policy Reference & Hierarchy

- This charter operates under the [Information Security Policy](./Information%20Security%20Policy.md) and is supported by related policies, standards, and procedures.

---

## Appendix

- References: [NIST SSDF](https://csrc.nist.gov/publications/detail/white-paper/2022/secure-software-development-framework/final), [OWASP](https://owasp.org/), ISO/IEC 27001:2022
- Version history is maintained in the Git commit log
