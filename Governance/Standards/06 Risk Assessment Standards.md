---
standard_ID: "S06"
title: "Risk Assessment Standards"
status: Draft       # Options: "Draft", "Approved", "Deprecated"  
document_owner: ""  
document_maintainer: ""  
last_approval: "YYYYMMDD"  
next_review: "YYYYMMDD"  
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
* Reviewed annually or upon significant changes.

## 7. References
- NIST RMF  
- [Risk Assessment Policy](../Policies/03\ Risk\ Assessment\ Policy.md) 

## 8. Audit & Traceability
- Compliance is verified through periodic reviews of implementation artifacts.
- Contributors may be asked to attest to adherence via signed commits or onboarding checklists.

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Risk | {{Definition}} |
| Risk Event | {{Definition}} |
| System Security and Privacy Plan | {{Definition}} |
| Security Assessment Report | {{Definition}} |



### B. Version History
Version history tracked via Git commit log.
