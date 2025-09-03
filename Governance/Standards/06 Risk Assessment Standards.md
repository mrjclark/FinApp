---
standard_ID: "S06"
title: "Risk Assessment Standards"
status: "Approved"       # Options: "Draft", "Approved", "Deprecated"  
document_owner: "mrjclark"  
document_maintainer: "mrjclark"  
last_approval: "20250903"  
next_review: "20260903"  
---

# Risk Assessment Standards

## 1. Purpose & Scope

### 1.1 Purpose
This document will establish the minimum requirements when conducting risk assessments for the FinApp project. It will be based on NIST's Risk Management Framework (RMF), and will include language on how to augment this with statistical probabilities in place of the use of ordinal scales.

### 1.2 Scope
This will be for all contributors who will be conducting a risk assessment for the entirety of the project, any of the critical functions supporting the project, or any of the assets for the project created through development. 

## 2. Roles & Responsibilities
| Role | Responsibilities |
|------|------------------|
| Project Lead | Responsible for identifying risk management roles, establishing risk tolerance strategy and governance, conducting and updating comprehensive risk assessment, creating project control baselines, and review findings from control implementations to inform future decisions. |
| Risk Owner | Responsible for documenting and publishing risk related controls, the confirmation of the categorization and prioritization of risks, and review findings from control implementations to inform future decisions. |
| Risk Lead | Responsible for assigning roles for executing RMF activities. |
| Risk Analyst | Responsible for carrying out the risk assessment. |

## 3. Standard Requirements
Each risk assessment will adhere to following minimum requirements for research and documentation when being developed.

### 3.1 Risk Assessment Life Cycle

#### 3.1.1 Preparation
- Identify and assign key roles for executing RMF activities.
- Establish a strategy that defines risk tolerance and governance.
- Conduct or update a comprehensive risk assessment.
- Create organization-specific control baselines or CSF profiles.
- Document and publish controls available for inheritance.
- Prioritize systems with similar impact levels.
- Define how control effectiveness will be monitored across systems.

#### 3.1.2 Categorization
- Document the system’s characteristics, boundaries, and purpose.
- Identify system components, data flows, and external connections.
- Align with enterprise architecture and project processes.
- Categorize the system and its information types by identifying the 90% confidence interval (CI) of the time to recover from any impacts related to a breach of confidentiality, integrity, or availability.i
    - The 90% CI must be defined using methods of industry expert judgement, historical data, or Monte Carlo simulations.
- Document results in the System Security and Privacy (SSP) Plan.
- Ensure categorization reflects the project's risk tolerance and strategy.
- The Risk Owner will review and formally approve the categorization decision.
- Ensure consistency with organizational risk posture and reporting requirements as per S05 Incident Handling Standards.

#### 3.1.3 Selection
- Base selection on system impact and likelihood calculations.
- Include both security and privacy controls.
- Remove non-applicable controls.
- Add controls to address specific threats or project needs.
- Apply overlays for specialized environments.
- Designate controls as:
  - System-specific: implemented directly in the system.
  - Common: inherited from shared infrastructure.
  - Hybrid: partially system-specific and partially common.
- Record selected and tailored controls in SSP Plan.
- Include rationale for tailoring and allocation decisions.
- A risk lead must review and approve selected controls.
- Ensure alignment with organizational risk tolerance and project needs.

#### 3.1.4 Implementation
- Configure and integrate controls into the system architecture.
- Ensure controls are implemented in accordance with design specifications.
- Document how each control is deployed and functions within the system.
- Coordinate with system engineers, administrators, and stakeholders during implementation.
- Prepare for control assessment by ensuring completeness and traceability.
- Update the System Security and Privacy Plan (SSPP), and related documentation to reflect implementation status.

#### 3.1.5 Assessment
- Conduct assessments to determine if controls are implemented properly and functioning as intended.
- Use independent assessors or assessment teams, especially for moderate or high-impact systems.
- Document assessment procedures, results, and findings.
- Identify weaknesses, deficiencies, or risks in control implementation.
- Update the Security Assessment Report (SAR) with detailed results.
- Support risk-based decisions for system authorization and continuous monitoring.

#### 3.1.6 Authorization
- Compile the authorization package, including the SSP Plan, SAR, and Plan of Action and Milestones (POA&M).
- Conduct a risk analysis based on assessment results and system context.
- Review privacy risks, especially for systems processing personally identifiable information (PII) and personal financial information (PFI).
- Present the authorization package to the Risk Owner (RO).
- RO evaluates the risk and makes an informed decision to authorize or deny implementation.
- Document the authorization decision and conditions for ongoing operation.

#### 3.1.7 Monitoring
- Continuously track the effectiveness of security and privacy controls using metrics and indicators.
- Detect changes to the system or environment that may affect risk posture.
- Conduct periodic assessments and automated scans where feasible.
- Update control implementation and documentation based on monitoring results.
- Maintain the POA&M to address identified weaknesses.
- Report findings to for informed decision-making.
- Support system reauthorization or ongoing authorization as needed.

### 3.2 Segregation of duties
- Where roles are combined, the project owner or applicable system RO shall review the roles request, and document any approvals and rationale
- Reviewers will analyze audit logs and report any deficiencies to the project owner or the applicable system RO. 
- When possible, contributors will implement automated controls and logs to support the review process.
- The project owner will perform a monthly review of the segregation of duties to ensure compliance with this policy.

## 4. Implementation Guidance
[Optional section for best practices, tooling suggestions, or links to procedures.]

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed annually or upon change in risk impacting a system.  

## 6. Review & Maintenance
 Reviewed annually or upon significant changes.

## 7. References
- NIST RMF  
- [Risk Assessment Policy](../Policies/03\ Risk\ Assessment\ Policy.md) 

## 8. Audit & Traceability
- Compliance is verified through periodic reviews of implementation artifacts.
- Contributors may be asked to attest to adherence via signed commits or onboarding checklists.

---

## Appendix
### Appendix A: Definitions
| Term                          | Definition |
|------------------------------|------------|
| Risk | The potential for an event to occur that could result in loss or disruption to the system, contributors, or project goals. |
| Risk Event | A specific occurrence or scenario that triggers a deviation from expected outcomes, impacting confidentiality, integrity, or availability. |
| System Security and Privacy Plan (SSPP) | A consolidated document that defines the system’s security and privacy controls, implementation status, and alignment with risk tolerance strategy. |
| Security Assessment Report (SAR) | A formal record of control assessments, including procedures, findings, and recommendations for authorization and continuous monitoring. |
| Confidence Interval (CI) | A statistical range (e.g., 90%) within which the true value of a metric (e.g., time to recover from impact) is expected to fall, based on available data. |
| Control Baseline | A predefined set of security and privacy controls tailored to the system’s categorization and risk tolerance. |
| Inherited Control | A control implemented by shared infrastructure or services and adopted by the system without direct implementation. |
| Hybrid Control | A control that is partially implemented by the system and partially inherited from shared infrastructure. |
| Plan of Action and Milestones (POA&M) | A document outlining identified weaknesses, planned remediation steps, responsible parties, and timelines for resolution. |
| Risk Tolerance Strategy | The documented approach for determining acceptable levels of risk, guiding control selection, prioritization, and authorization decisions. |
| Audit Artifact | Any documented evidence (e.g., logs, checklists, signed commits) used to verify compliance with risk assessment standards. |
| Calibrated Estimation | A method of expert judgment refined through training and feedback to produce statistically meaningful estimates with confidence intervals. |
| Monte Carlo Simulation | A computational technique that models the probability of different outcomes by running simulations using random variables. |
| Impact Recovery Time | The estimated duration required to restore system functionality and contributor trust following a breach or disruption. |
| Confidence-Weighted Prioritization | A method for ranking risks or controls based on both expected impact and confidence in the estimate. |
| Contributor Churn Risk | The probability that contributors disengage due to trust erosion, burnout, or breach-related stress. |
| Control Traceability Matrix | A structured mapping of controls to system components, responsible roles, and audit artifacts. |

### B. Version History
Version history tracked via Git commit log.
