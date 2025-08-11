---
policy_ID: "P03"
title: "Risk Assessment Policy"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# Risk Assessment Policy

## 1. Purpose & Scope

### 1.1 Purpose
To establish a consistent and effective approach for identifying, assessing, treating, and monitoring information security risks throughout the FinApp project lifecycle, in line with NIST Risk Management Framework (RMF) requirements, as well as the implementation of NIST SP 800-53 controls to support risk assessments.

### 1.2 Scope
This policy applies to all information assets, technology components, development activities, and supporting processes within the FinApp project.

## 2. Policy Statement
FinApp is committed to proactively identifying and managing risks that may impact the confidentiality, integrity, and availability of its information assets and services. Risk assessment is integral to the secure software development lifecycle and ongoing project management.

## 3. Policy Objectives
- Ensure consistent identification and assessment of information security risks.
- Support informed decision-making for risk treatment and control selection.
- Maintain compliance with NIST RMF and NIST SP 800-53 requirements.
- Protect the confidentiality, integrity, and availability of information assets.
- Promote continual improvement of risk management practices.

## 4. Roles and Responsibilities

### 4.1 Key Roles
| Role | Responsibilities |
| --- | --- |
| Project Lead (Owner, System Owner, Authorizing Official) | Accountable for policy creation, review, and enforcement. Approves risk acceptance and ensures adequate resources for security. Oversees system development and authorization decisions. |
| Contributors (System Security Engineers, Users) | Execute secure development tasks. Follow security policies and report anomalies. Participate in training and implement assigned controls. |
| Reviewers/Auditors (Security Control Assessors) | Independently assess controls, review audit logs, and report deficiencies. Support authorization decisions and continuous improvement. |
| Third Parties (External Providers, Common Control Providers) | Deliver services or components under agreed security requirements. Participate in supply chain reviews and maintain inherited controls. |

 
### 4.2 Segregation of duties
- Where roles are combined, the project owner shall review the roles request, and document any approvals and rationale
- Reviewers will review audit logs and report any deficiencies to the project owner. 
- When possible, contributors will implement automated controls and logs to support the review process.
- The project owner will perform a monthly review of the segregation of duties to ensure compliance with this policy.

## 5. Risk Assessment Process

### 5.1 Preparation
- Identify and assign key roles for executing RMF activities.
- Establish a strategy that defines risk tolerance and governance.
- Conduct or update a comprehensive risk assessment.
- Create organization-specific control baselines or CSF profiles.
- Document and publish controls available for inheritance.
- Prioritize systems with similar impact levels.
- Define how control effectiveness will be monitored across systems.

### 5.2 Categorization
- Document the system’s characteristics, boundaries, and purpose.
- Identify system components, data flows, and external connections.
- Align with enterprise architecture and mission/business processes.
- Categorize the system and its information types using:
- FIPS 199 for impact levels (Low, Moderate, High)
- NIST SP 800-60 for mapping information types
- Document results in the system security plan (SSP), privacy plan, and supply chain risk management (SCRM) plan.
- Ensure categorization reflects the organization’s risk tolerance and strategy.
- Senior leaders review and formally approve the categorization decision.
- Ensure consistency with organizational risk posture and reporting requirements.

### 5.3 Selection

- Select initial control set from NIST SP 800-53B.
- Base selection on system impact level (Low, Moderate, High).
- Include both security and privacy controls.
- Remove non-applicable controls.
- Add controls to address specific threats or project needs.
- Apply overlays for specialized environments.
- Designate controls as:
  - System-specific: implemented directly in the system.
  - Common: inherited from shared infrastructure.
  - Hybrid: partially system-specific and partially common.
- Record selected and tailored controls in:
  - System Security Plan (SSP)
  - Privacy Plan
  - Supply Chain Risk Management (SCRM) Plan
- Include rationale for tailoring and allocation decisions.
- Senior officials review and approve selected controls.
- Ensure alignment with organizational risk tolerance and mission needs.

### 5.4 Implementation
- Configure and integrate controls into the system architecture.
- Ensure controls are implemented in accordance with design specifications.
- Document how each control is deployed and functions within the system.
- Coordinate with system engineers, administrators, and stakeholders during implementation.
- Prepare for control assessment by ensuring completeness and traceability.
- Update the System Security Plan (SSP), Privacy Plan, and related documentation to reflect implementation status.

### 5.5 Assessment
- Conduct assessments to determine if controls are implemented properly and functioning as intended.
- Use independent assessors or assessment teams, especially for moderate or high-impact systems.
- Document assessment procedures, results, and findings.
- Identify weaknesses, deficiencies, or risks in control implementation.
- Update the Security Assessment Report (SAR) with detailed results.
- Support risk-based decisions for system authorization and continuous monitoring.

### 5.6 Authorization
- Compile the authorization package, including the System Security Plan (SSP), Security Assessment Report (SAR), and Plan of Action and Milestones (POA&M).
- Conduct a risk analysis based on assessment results and system context.
- Review privacy risks, especially for systems processing personally identifiable information (PII).
- Present the authorization package to the Authorizing Official (AO).
- AO evaluates the risk and makes an informed decision to authorize or deny system operation.
- Document the authorization decision and conditions for ongoing operation.

### 5.7 Monitoring
- Continuously track the effectiveness of security and privacy controls using metrics and indicators.
- Detect changes to the system or environment that may affect risk posture.
- Conduct periodic assessments and automated scans where feasible.
- Update control implementation and documentation based on monitoring results.
- Maintain the Plan of Action and Milestones (POA&M) to address identified weaknesses.
- Report findings to stakeholders and Authorizing Officials for informed decision-making.
- Support system reauthorization or ongoing authorization as needed.

## 6. Reporting and Escalation
- All identified risks and treatment decisions are documented.
- Security incidents or new significant risks are reported to the project owner for review and response.

## 7. Policy Review
- This policy is reviewed annually or following significant changes to the project or threat landscape.

## 8. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 9. Review & Maintenance
* Reviewed annually or upon significant changes.

## 10. References
- [NIST RMF](https://csrc.nist.gov/Projects/Risk-Management)
- [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [NIST SP 800-53B](https://csrc.nist.gov/publications/detail/sp/800-53b/final)
- [NIST SP 800-60](https://csrc.nist.gov/publications/detail/sp/800-60/rev-1/final)
- [NIST SP 800-37](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)

---

## Appendix

### A. Definitions
| Term | Definition |
|---|---|
| Risk Management Framework (RMF) | A structured process for managing security and privacy risk that integrates with the system development life cycle. |
| System Security Plan (SSP) | A formal document that describes the security controls in place or planned for an information system. |
| Security Assessment Report (SAR) | A report detailing the results of assessing the effectiveness of security controls. |
| Plan of Action and Milestones (POA&M) | A document identifying tasks to correct deficiencies and reduce or eliminate vulnerabilities. |
| Privacy Plan | A document outlining privacy controls and how they are implemented to protect personally identifiable information (PII). |
| Categorization | The process of determining the impact level of a system based on the sensitivity of the information it processes. |

### B. Version History
Version history is maintained in the Git commit log.

