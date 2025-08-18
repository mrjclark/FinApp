---
standard_ID: "S06"
title: "Risk assessment Standards"
status: Draft       # Options: "Draft", "Approved", "Deprecated"  
document_owner: ""  
document_maintainer: ""  
last_approval: "YYYYMMDD"  
next_review: "YYYYMMDD"  
---

# Risk Assessment Standards

## 1. Purpose & Scope

### 1.1 Purpose
This document will establish the minimum requirements when conducting risk assessments for the FinApp project. It will be based NIST's Risk Management Framework (RMF), and will include language on how to augment this with statical probabilities in place of the use of ordinal scales.

### 1.2 Scope
This will be for all contributors who will be conducting a risk assessment for the entirety of the project, any of the critical functions supporting the project, or any of the assets for the project created through development. 

## 2. Roles & Responsibilities
List key roles and what they’re expected to do.
| Role | Responsibilities |
|------|------------------|
| Project Lead | Responsible for identifying risk management roles, establishing risk tolerance strategy and governance, conducting and updating comprehensive risk assessment, and creating project control baselines. |
| Risk Owner | Responsible for documenting and publishing risk related controls, the confirmation of the categorization and prioritization of risks,   |
| Risk Lead | Responsible for assigning roles for executing RMF activities |
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
- Align with enterprise architecture and mission/business processes.
- Categorize the system and its information types using:
    - FIPS 199 for impact levels (Low, Moderate, High)
    - NIST SP 800-60 for mapping information types
- Document results in the system security plan (SSP), privacy plan, and supply chain risk management (SCRM) plan.
- Ensure categorization reflects the organization’s risk tolerance and strategy.
- The Risk Owner will review and formally approve the categorization decision.
- Ensure consistency with organizational risk posture and reporting requirements as per S05 Incident Handling.

#### 3.1.3 Selection
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

#### 3.1.4 Implementation
- Configure and integrate controls into the system architecture.
- Ensure controls are implemented in accordance with design specifications.
- Document how each control is deployed and functions within the system.
- Coordinate with system engineers, administrators, and stakeholders during implementation.
- Prepare for control assessment by ensuring completeness and traceability.
- Update the System Security Plan (SSP), Privacy Plan, and related documentation to reflect implementation status.

#### 3.1.5 Assessment
- Conduct assessments to determine if controls are implemented properly and functioning as intended.
- Use independent assessors or assessment teams, especially for moderate or high-impact systems.
- Document assessment procedures, results, and findings.
- Identify weaknesses, deficiencies, or risks in control implementation.
- Update the Security Assessment Report (SAR) with detailed results.
- Support risk-based decisions for system authorization and continuous monitoring.

#### 3.1.6 Authorization
- Compile the authorization package, including the System Security Plan (SSP), Security Assessment Report (SAR), and Plan of Action and Milestones (POA&M).
- Conduct a risk analysis based on assessment results and system context.
- Review privacy risks, especially for systems processing personally identifiable information (PII).
- Present the authorization package to the Authorizing Official (AO).
- AO evaluates the risk and makes an informed decision to authorize or deny system operation.
- Document the authorization decision and conditions for ongoing operation.

#### 3.1.7 Monitoring
- Continuously track the effectiveness of security and privacy controls using metrics and indicators.
- Detect changes to the system or environment that may affect risk posture.
- Conduct periodic assessments and automated scans where feasible.
- Update control implementation and documentation based on monitoring results.
- Maintain the Plan of Action and Milestones (POA&M) to address identified weaknesses.
- Report findings to stakeholders and Authorizing Officials for informed decision-making.
- Support system reauthorization or ongoing authorization as needed.

### 3.2 Segregation of duties
- Where roles are combined, the project owner shall review the roles request, and document any approvals and rationale
- Reviewers will review audit logs and report any deficiencies to the project owner. 
- When possible, contributors will implement automated controls and logs to support the review process.
- The project owner will perform a monthly review of the segregation of duties to ensure compliance with this policy.

## 4. Implementation Guidance
[Optional section for best practices, tooling suggestions, or links to procedures.]

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.  

## 6. Review & Maintenance
* Reviewed annually or upon significant changes.

## 7. References
- NIST [Relevant Publications]  
- OWASP / CIS / Additional frameworks  
- Internal policy or repo links (if applicable)

## 8. Audit & Traceability
- Compliance is verified through periodic reviews of implementation artifacts.
- Contributors may be asked to attest to adherence via signed commits or onboarding checklists.

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| {{Term}} | {{Definition}} |

### B. Version History
Version history tracked via Git commit log.
