---
title: "Initial Organizational Risk Assessment"
status: "Draft"
version: "0.1"
author: "mrjclark"
date_created: ""
last_updated: ""
tags:
  - finapp
  - security-assessment
external_linked_controls:
  nist:
    - "SP 800-30 Rev. 1"
    - "SP 800-37"
  cis:
  owasp:
related_documents:
  - "[Document Name](Document link)"
contributor_roles:
  - "[Who is this audience]"
---
• Identify the purpose of the assessment;
• Identify the scope of the assessment;
• Identify the assumptions and constraints associated with the assessment;
• Identify the sources of information to be used as inputs to the assessment; and
• Identify the risk model and analytic approaches (i.e., assessment and analysis approaches) to 
be employed during the assessment.

# High-Level Risk Assessment

## Purpose
## Tier 1 Initial Risk Assessment Purpose Statement
This initial Tier 1 risk assessment aims to identify strategic threats, threat sources, and systemic vulnerabilities that may impact the decentralized development and stewardship of our personal finance and budgeting application. As the first formal risk evaluation for this project, it establishes a baseline understanding of organizational risk posture, informs symbolic governance and contributor onboarding, and guides the prioritization of security and privacy controls. The assessment aligns with NIST SP 800-37 and SP 800-30 guidance, supporting risk-informed decision-making and laying the foundation for continuous monitoring and future Tier 2 and Tier 3 assessments.

## Scope
This Tier 1 risk assessment applies to the entire decentralized development project for the personal finance and budgeting application. It encompasses all assets produced during development, including source code, documentation, contributor workflows, and governance artifacts.

The assessment evaluates strategic risks associated with:
- Software development practices and lifecycle transitions
- Small team dynamics and contributor onboarding
- Handling and storage of personal financial data

The scope includes both security and privacy risks, in alignment with NIST SP 800-30 Rev. 1 and SP 800-37 Rev. 2. It supports organizational-level decision-making, control selection, and symbolic stewardship rituals.

This assessment remains valid for one (1) year from approval unless one or more of the following conditions occur:
- The project transitions from development to operational deployment
- The contributor team exceeds ten (10) personnel
- The project begins handling or storing data types beyond personal financial data

Any of these changes will trigger a reassessment to ensure continued alignment with RMF guidance and evolving risk posture.

## Assumptions and Constraints
### Assumptions
- Threat actors are expected to be less capable and primarily opportunistic, rather than targeted or persistent.
- All contributors will adhere to formal code review protocols and automated code scanning requirements.
- Contributors are assumed to be self-motivated to internalize and uphold project values, including symbolic governance rituals.
- Third-party contributions will undergo additional risk assessments prior to integration.
- Contributors will maintain stable access to infrastructure, tooling, and communication channels.
- Personally identifiable information (PII) will be minimized; names, emails, and other identifiers will not be collected.
- Personal financial information (PFI) will exclude bank credentials or sensitive financial identifiers; all data will be operational in nature.
- Contributors will be required to sign commits and use multi-factor authentication (MFA) for audits and peer reviews.
- No formal legal or regulatory oversight is expected during development; internal audits will serve as the primary assurance mechanism.
- Governance rituals and stewardship protocols will be introduced during onboarding and reaffirmed annually

### Constraints
- Time for initial implementation and risk assessment is limited to one (1) week.
- Personnel is currently limited to a single steward; expansion to ten (10) contributors will materially affect the risk posture.
- Tooling and automation capabilities will be constrained by the technical proficiency of contributors.
- External consultations will only be pursued through available, no-cost services or community support.
- Contributors will be responsible for implementing and maintaining assigned controls.
- Governance authority resides solely with the project owner; all decisions, rituals, and standards are stewarded centrally.
- Data will be classified (e.g., operational, symbolic, audit-relevant) and handled according to predefined protocols.
- The project must remain open-source; no monetization of this project or derivative works will be permitted.

## Threats
### Threats Derived from Assumptions

1. Underestimated Threat Actor Capability
- Assumption: Threat actors are opportunistic and less capable.
- Threat: A more sophisticated attacker targets the app due to its open-source nature or symbolic visibility.

2. Contributor Misalignment or Burnout
- Assumption: Contributors are self-motivated to uphold values.
- Threat: Misalignment with governance rituals or contributor disengagement leads to inconsistent control implementation or symbolic drift.

3. Third-Party Component Risk
- Assumption: All third-party contributions will be vetted.
- Threat: A dependency is integrated before full vetting, introducing vulnerabilities or licensing conflicts.

4. Stable Access Disruption
- Assumption: Contributors have stable access.
- Threat: Infrastructure outages, contributor relocation, or account lockouts disrupt development or audits.

5. Minimal PII and PFI Exposure
- Assumption: No sensitive identifiers or bank data will be collected.
- Threat: A misconfigured form or logging mechanism inadvertently captures sensitive data.

### Threats Derived from Constraints

6. Single Steward Bottleneck
- Constraint: Only one person conducting the assessment.
- Threat: Blind spots in threat modeling, limited validation, or delayed response to emerging risks.

7. Team Growth Impact
- Constraint: Risk posture changes at 10+ contributors.
- Threat: Rapid onboarding without governance alignment introduces insider risk or control gaps.

8. Limited Tooling and Automation
- Constraint: Technical knowledge limits automation.
- Threat: Manual processes fail to detect vulnerabilities, misconfigurations, or audit gaps.

9. Free-Only External Consultation
- Constraint: Only free services will be used.
- Threat: Lack of expert validation or delayed response to high-risk findings due to resource constraints.

10. Contributor-Control Dependency
- Constraint: Contributors must implement controls.
- Threat: Controls are inconsistently applied or misunderstood, especially in symbolic or emotional domains.

11. Open-Source Exposure
- Constraint: Project must remain open-source and non-monetized.
- Threat: Public visibility increases attack surface; lack of monetization may limit incentives for long-term maintenance.

