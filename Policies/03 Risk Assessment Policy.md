# Risk Assessment Policy
Document Status: Draft

## 1. Purpose & Scope

### 1.1 Purpose
To establish a consistent and effective approach for identifying, assessing, treating, and monitoring information security risks throughout the FinApp project lifecycle, in line with ISO/IEC 27001:2022 requirements.

### 1.2 Scope
This policy applies to all information assets, technology components, development activities, and supporting processes within the FinApp project.

## 2. Policy Statement
FinApp is committed to proactively identifying and managing risks that may impact the confidentiality, integrity, and availability of its information assets and services. Risk assessment is integral to the secure software development lifecycle and ongoing project management.

## 3. Policy Objectives
- Ensure consistent identification and assessment of information security risks.
- Support informed decision-making for risk treatment and control selection.
- Maintain compliance with ISO/IEC 27001:2022 requirements.
- Protect the confidentiality, integrity, and availability of information assets.
- Promote continual improvement of risk management practices.

## 4. Roles and Responsibilities
| Role                | Responsibilities                                                                 |
|---------------------|----------------------------------------------------------------------------------|
| Owner / Project Lead| Approves risk assessment methodology, reviews outcomes, accepts residual risk.    |
| Lead Developer      | Conducts risk assessments, documents results, implements controls.                |

- Segregation of duties: Where roles are combined, the project owner approves all responsibilities and documents this as a compensating control.

## 5. Risk Assessment Process

### 5.1 Identification
- Identify assets, vulnerabilities, and potential impacts at each SDLC stage and for any significant change.
- Use industry-recognized frameworks for asset and vulnerability identification.

### 5.2 Assessment
- Evaluate risks based on likelihood and impact (qualitative/semi-quantitative as appropriate).
- Document risks in a risk register, including owner and mitigation status.

### 5.3 Risk Treatment
- Determine appropriate treatment: mitigate, transfer, avoid, or accept.
- Select and implement controls based on risk level and business context.
- Document acceptance of residual risk by the project owner.

### 5.4 Monitoring and Review
- Review and update the risk register at least annually or upon significant project changes.
- Reassess risks after security incidents or major releases.
- Maintain records of all assessments, decisions, and implemented controls.

## 6. Reporting and Escalation
- All identified risks and treatment decisions are documented.
- Security incidents or new significant risks are reported to the project owner for review and response.

## 7. Policy Review
- This policy is reviewed annually or following significant changes to the project or threat landscape.

---

## Appendix

### A. Version History
Version history is maintained in the Git commit log.

### B. References
- ISO/IEC 27001:2022, Clauses 6.1.2, A.8.2, A.6.1
- NIST SP 800-30

### C. Definition of Information Security Risk
Information security risk is the potential for loss, damage, or disruption to information assets resulting from the occurrence of a threat exploiting a vulnerability. It is typically measured by considering the likelihood of an event and the impact it would have on the confidentiality, integrity, or availability of information.