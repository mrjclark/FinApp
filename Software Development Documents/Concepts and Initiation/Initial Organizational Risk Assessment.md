---
title: "Initial Organizational Risk Assessment"
status: "Approved"
version: "1.0"
author: "mrjclark"
date_created: "20250810"
last_updated: "20260810"
tags:
  - finapp
  - security-assessment
related_documents:
  - "[Document Name](Document link)"
contributor_roles:
  - "Project Lead"
  - "Auditors"
  - "Security Engrineer"
  - "DevSecOps Lead"
  - "Risk Analyst"
  - "Contributor Onboarder"
  - "Third-Party Representative"
---

# High-Level Risk Assessment

## Purpose
## Tier 1 Initial Risk Assessment Purpose Statement
This initial Tier 1 risk assessment aims to identify strategic threats, threat sources, and systemic vulnerabilities that may impact the decentralized development and stewardship of our personal finance and budgeting application. As the first formal risk evaluation for this project, it establishes a baseline understanding of organizational risk posture, informs symbolic governance and contributor onboarding, and guides the prioritization of security and privacy controls. The assessment aligns with NIST SP 800-37 and SP 800-30 guidance, supporting risk-informed decision-making and laying the foundation for continuous monitoring and future Tier 2 and Tier 3 assessments.

Importantly, this project is intentionally designed to remain non-monetized, with no expectation of revenue generation or financial profit. As such, traditional risk models that estimate expected monetary loss are not applicable. Instead, this assessment adopts a combined qualitative and quantitative approach, where the primary loss metric is time—specifically, the time required to recover from a given impact. This time-centric model aligns with the project’s symbolic governance philosophy and supports decision-making based on stewardship effort, operational continuity, and contributor experience, rather than financial cost.

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

## Information Sources
Information sources will be external to the project. Information for this initial risk assessment has come from:
- NIST Special Publications
- OWASP
- CIS
- MITRE
- Hubbard & Seiersen

## Time-Based Impact Modeling
Each risk scenario is assessed using:

- Likelihood (Low / Medium / High or probabilistic range)
- Qualitative Impact (e.g., trust erosion, audit failure, contributor misalignment)
- Quantitative Impact (estimated time-to-recovery in hours or days)

## Risk Model and Analytic Approach
This Tier 1 risk assessment employs a vulnerability-oriented risk model, consistent with NIST SP 800-30 Rev. 1 guidance. The analytic approach includes:

- Qualitative analysis of symbolic, emotional, and operational impacts
- Quantitative modeling using time-to-recovery (TTR) as a proxy for loss
- Calibrated expert judgment, Bayesian inference, and Monte Carlo simulation to estimate likelihood and time-based impact distributions

This hybrid approach enables prioritization of controls based on recovery burden, contributor alignment, and symbolic governance integrity.

### Threat Sources
Based on the threats from the assumptions and constraints, the likely sources of threat to the project will be as follows:

#### Adversarial
- Opportunistic attackers targeting open-source or financial applications
- Malicious insiders or disgruntled contributors
- Supply chain risks from compromised third-party libraries or dependencies
- Credential stuffing or brute-force attempts against contributor accounts

#### Accidental
- Contributor misconfiguration or commit errors
- Failure to follow onboarding or governance rituals
- Unintended data exposure due to logging, form design, or misused variables
- Overly permissive access controls or forgotten cleanup steps

#### Structural
- Limited automation or tooling failures during CI/CD or deployment
- Dependency on unstable or poorly maintained libraries
- Single steward bottlenecks in decision-making or control implementation
- Inadequate versioning or rollback mechanisms

#### Environmental
- Infrastructure outages (e.g., cloud service disruptions or DNS failures)
- Localized power or connectivity issues affecting contributor availability
- Natural events impacting hosting or contributor access
- Heat-related hardware degradation or thermal throttling on local systems

### Threat Events
- Perform perimeter network reconnaissance/scanning
- Craft phishing attacks
- Craft attacks specifically based on deployed IT environment
- Deliver known malware to internal organization info systems
- Insert untargeted malware into downloadable software
- Exploit physical access of authorized contributors to gain access to project assets
- Exploit poorly configured or unauthorized system exposed to the internet
- Exploit multi-tenancy in a cloud environment
- Exploit recently discovered vulnerabilities 
- Exploit misconfigured roles or permissions
- Conduct communications interception attacks
- Conduct attacks using unauthorized ports, protocols, or services
- Conduct brute force login attempts/password stuffing attacks
- Conduct externally-based session hijacking
- Conduct externally-based man in the middle attacks
- Conduct supply chain attacks
- Conduct attacks using denial of service targeting availability of contributor infrastructure or CI/CD pipelines
- Conduct attack using and authorized contributor to intentionally bypassing controls
- Obtain sensitive information via exfiltration (API keys, user keys)
- Cause integrity loss by polluting or corrupting critical data
- Obtain unauthorized access

### Vulnerabilities
- Lack of automated dependency scanning or vulnerability patching
- Inadequate rate limiting on CI/CD triggers or API endpoints
- Absence of formal contributor access reviews or role separation
- Limited logging or monitoring of contributor actions and pipeline events
- Overreliance on governance without technical enforcement
- Incomplete validation of third-party libraries or open-source contributions
- No formal secrets management or token rotation process
- Small team size and limited operational redundancy
- Open-source exposure with public visibility of code and workflows
- Decentralized governance with enforcement rather than centralized control
- Limited external consultation and tooling due to resource constraints
- High reliance on contributor self-motivation and governance adherence
- No formal legal or regulatory oversight to enforce compliance
- Project philosophy prohibits monetization, reducing incentives for long-term maintenance

### Likelihood of Exploitations

#### Quantitative Risk Estimation Methodology
Likelihood estimates for identified risk scenarios are derived using probabilistic modeling techniques outlined in How to Measure Anything in Cybersecurity Risk by Douglas W. Hubbard and Richard Seiersen (Wiley, 2nd Edition, 2023). This approach emphasizes calibrated expert judgment, Bayesian inference, and Monte Carlo simulation to quantify uncertainty and improve decision accuracy.

Reference:
Hubbard, D. W., & Seiersen, R. (2023). How to Measure Anything in Cybersecurity Risk (2nd ed.). Wiley. ISBN: 978-1-119-89230-4

### Impacts
#### Harm to Individuals
- Loss of PII or PFI
- Damage to image or reputation

#### Harm to Mission
- Disruption of contributor alignment
- Failure to meet transparency or auditability expectations

#### Harm to Operations
- Inability to perform project development with sufficient confidence and/or correctness
- Harm due to noncompliance with internal requirements
- Damage to trust relationships

#### Harm to Assets
- Loss or corruption of audit artifacts (e.g., contributor logs, symbolic tags, control mappings)
- Unauthorized modification of contributor standards, or onboarding covenants

#### Harm to External Stakeholders
- Loss of credibility with auditors, partners, or external collaborators
- Exposure of sensitive artifacts

### Determine Risk
Risk was calculated by integrating likelihood and impact estimates for each scenario:

- Risk rankings were modeled using the likelihood times a weighted average of the upper and lower bounds of the 90% confidence interval of the impact to the time to recovery in hours
- Scenarios were ranked by expected value and tail risk to inform control prioritization.
- Results will guide governance updates, contributor onboarding, and control implementation.

This risk determination supports Tier 1 strategic decision-making and lays the foundation for future Tier 2 and Tier 3 assessments.

Risk is calculated as:
$$
\text{Risk Ranking} = \text{Likelihood} \times \left(0.65 \times \text{Upper Bound} + 0.35 \times \text{Lower Bound}\right)
$$
This produces a time-weighted risk register that supports prioritization of controls, governance updates, and contributor onboarding rituals.

| Threat Event | Likelihood | Lower Bound | Upper Bound | Notes and Sources | Risk Ranking |
| ------------ | ---------- | ----------- | ----------- | ----------------- | ------------ |
| Perform perimeter network reconnaissance/scanning | 0.8 | 0.1 | 2 | 0.612 | NIST SP 800-30 Rev. 1 states scanning is common<br>Censys and Shodan scan public IP's daily<br>Hubbard & Seiersen calibrated expert judgment for high-frequency, low impact events |
| Craft phishing attacks | 0.6 | 0.5 | 4 | 1.035 | OWASP top threat vector<br>Hubbard & Seiersen expert calibrated judgement for similar organizations |
| Craft attacks specifically based on deployed IT environment | 0.4 | 1 | 6 | 1.1 | NIST SP 800-30 Rev.1 estimate for environment-specific attacks that are dependent on exposure<br>Hubbard & Seiersen reference for forecasting of similar CI/CD setups |
| Deliver known malware to internal organization info systems | 0.3 | 2 | 12 | 1.65 | OWASP shows malware delivery is common through email or downloads<br>Hubbard & Seiersen estimate based on contributor hygene and scanning controls |
| Insert untargeted malware into downloadable software | 0.5 | 1 | 8 | 1.725 | NIST SP 800-30 Rev. 1 common risk in open-source ecosystems<br>Hubbard & Seiersen use of analogs from npm, PyPI, and GitHub incidents |
| Exploit physical access of authorized contributors | 0.1 | 1 | 6 | 0.275 | NIST SP 800-30 low-frequency unless shared workspaces are used |
| Exploit poorly configured or unauthorized internet-exposed systems | 0.7 | 2 | 10 | 3.36 | OWASP and Censys data show frequent scanning and exploitation of exposed ports. |
| Exploit multi-tenancy in a cloud environment | 0.2 | 1 | 8 | 0.69 | NIST SP 800-30 conditional on architecture. |
| Exploit recently discovered vulnerabilities | 0.6 | 2 | 12 | 3.3 | CVE data and Hubbard & Seiersen's reference class forecasting support elevated likelihood. |
| Exploit misconfigured roles or permissions | 0.5 | 1 | 6 | 1.375 | NIST SP 800-53 and OWASP highlight access control misconfigurations as top risks. |
| Exploit vulnerable third-party dependency | 0.6 | 2 | 8 | 2.46 | SBOM and CVE data show frequent exposure<br>OWASP and NIST recommend automated dependency scanning. |
| Exploit insecure default configurations | 0.5 | 1 | 6 | 1.375 | CIS benchmarks highlight default misconfigurations as systemic risks. |
| Exploit lack of input validation | 0.4 | 2 | 10 | 1.92 | OWASP Top 10 ranks injection and validation flaws as critical<br>mitigated by secure coding and automated testing. |
| Exploit lack of output encoding | 0.8 | 1 | 6 | 2.2 | MITRE CWE-116 ranks this as highly likely, though this needs to be chained with other exploits |
| Exploit lack of authentication or session management | 0.5 | 2 | 12 | 2.75 | OWASP and NIST SP 800-63 highlight session mismanagement as a top attack vector; common in MVP-stage apps. |
| Conduct communications interception attacks | 0.3 | 1 | 6 | 0.825 | NIST SP 800-30 lists interception as a moderate threat |
| Conduct attacks using unauthorized ports, protocols, or services | 0.4 | 2 | 8 | 1.64 | OWASP and CIS benchmarks highlight exposed services as common misconfigurations<br>Risk increases with public CI/CD endpoints and default configurations. |
| Conduct brute force login/password stuffing attacks | 0.5 | 1 | 6 | 1.375 | OWASP and NIST industry prevalence of this type of attack |
| Conduct externally-based session hijacking | 0.2 | 1 | 6 | 0.55 | OWASP data suggests this is less frequent than brute force or credential stuffing attacks but does have a similar impact |
| Conduct externally-based man-in-the-middle attacks | 0.1 | 1 | 12 | 0.485 | NIST IR 8286A gives a calibrated risk estimation using historical data |
| Conduct supply chain attacks | 0.8 | 4 | 24 | 8.8 | OWASP shows this to be a high probability occurrance, while recovery could take longer due to reviewing uses of any third-party resources |
| Conduct attacks using denial of service targeting availability of contributor infrastructure or CI/CD pipelines | 0.8 | 2 | 8 | 3.24 | Based on industry telemetry from Cloudflare |
| Conduct attack using an authorized contributor to intentionally bypassing controls | 0.5 | 4 | 10 | 3.05 | Verizon DBIR and Ponemon show insider breaches are in this range<br>The time required to discover and react is highly variable |
| Obtain sensitive information via exfiltration (API keys, user keys) | 0.9 | 2 | 12 | 4.95 | Cybelangel reports almost all organizations have sensitive API related information stolen<br>Time for recover could be key rotation or completely re-designing secure code in a particular asset. |
| Cause integrity loss by polluting or corrupting critical data | 0.5 | 2 | 10 | 2.4 | NIST list this as a common in software development environments<br>The impact is affected by times for restoring good backups. |
| Obtain unauthorized access | 0.7 | 4 | 20 | 6.72 | OWASP and NIST treat this as foundational risk<br>The impact is based on discovery and cleanup of any actions. |

## Risk Assessment Executive Summary
This Tier 1 risk assessment establishes a strategic baseline for FinApp’s decentralized development initiative, focusing on time-to-recovery (TTR) as the primary loss metric. Rather than financial cost, risks are ranked by their potential to disrupt the ability to uphold project confidentiality and integrity goals, contributor alignment, and operational continuity. The assessment integrates NIST SP 800-30, SP 800-37, OWASP, CIS, and Hubbard-style calibrated estimation to model both adversarial and accidental threats.


### Top-Ranked Risks by Time-Weighted Impact
| Threat Event | Risk Ranking (TTR-weighted) |
|--------------|-----------------------------|
| Supply chain attacks | 8.80 |
| Unauthorized access | 6.72 |
| Sensitive data exfiltration (API keys, user keys) | 4.95 |
| Insider control bypass | 3.05 |
| Exploiting exposed systems | 3.36 |
| Denial of service on contributor infra | 3.24 |
| Recently discovered vulnerabilities | 3.30 |

These risks pose the greatest threat to contributor trust, audit integrity, and symbolic governance. They are amplified by open-source exposure, small team size, and limited automation.


### Recommended Control Priorities
#### Identity and Access Management
- Enforce MFA and credential rotation
- Audit dormant accounts and service identities
- Implement JIT access and role separation

#### Secrets and Artifact Integrity
- Use Sigstore or similar for artifact signing
- Automate secret scanning and token rotation
- Harden CI/CD pipelines against exfiltration

#### Supply Chain and Dependency Hygiene
- Automate SBOM generation and vulnerability scanning
- Pin dependencies and validate third-party contributions
- Monitor for tampering in upstream libraries

#### Governance and Contributor Stewardship
- Ritualize onboarding with symbolic covenants
- Reaffirm governance protocols annually
- Use reflection cards to align emotional and operational intent

#### Monitoring and Recovery
- Implement audit logging for contributor actions
- Define rollback and recovery playbooks
- Simulate breach scenarios to validate TTR estimates

### Strategic Focus
This assessment supports FinApp’s governance model by translating technical risks into stewardship opportunities. Controls should prioritize:
- Preserving contributor and user trust
- Maintaining audit traceability
- Minimizing recovery time

As the project scales, future Tier 2 and Tier 3 assessments will refine these estimates and introduce continuous monitoring rituals.

## References
1. NIST SP 800-30 Rev. 1 – Guide for Conducting Risk Assessments.  
   National Institute of Standards and Technology, September 2012.  
   [https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final)

2. OWASP Top 10 – A08:2021 Software and Data Integrity Failures.  
   OWASP Foundation.  
   [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/)

3. CIS Controls v8 – Center for Internet Security.  
   [https://www.cisecurity.org/controls/cis-controls-list/](https://www.cisecurity.org/controls/cis-controls-list/)

4. Hubbard & Seiersen (2016) – How to Measure Anything in Cybersecurity Risk.  
   Wiley Publishing. ISBN: 978-1119085294

5. NIST SP 800-37 Rev. 2 – Risk Management Framework for Information Systems and Organizations.  
   [https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final](https://csrc.nist.gov/publications/detail/sp/800-37/rev-2/final)
