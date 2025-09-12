---
title: "Requirements Context"
status: "Draft"
version: "0.1"
author: "mrjclark"
date_created: "20250908"
last_updated: "20250908"
tags:
  - @requirements
  - @contributor-onboarding
external_linked_controls:
  nist:
    - "[SP #]:[Control:Section]"
  cis:
    - "[Control Section]"
  owasp:
    - "[Document Name]:[Section]"
related_documents:
  - "[Document Name](Document link)"
contributor_roles:
  - "Contributors"
  - "SecOps"
  - "Auditors"
---

# Requirement Document

## 1. Purpose and Scope

### 1.1 Purpose


Purpose Statement: FinApp provides secure, transparent, and compliant financial transaction management for small-to-medium enterprises, with built-in audit and reporting capabilities. 

## 1.2 Scope: 

### 1.2.1 In Scope:
This document will cover various requirements.
- Core features and functions to be delivered in this release. 
- Supported platforms, environments, and user groups. 
- Specify security and privacy requirements, both functional and non-functional.
- Create cyber resiliency objectives for anticipating, withstanding, recovering, and adapting.
- Align requirements with mission assurance and ethical commitments.
- Document all assumptions, constraints, and trade-offs transparently.
- Identify applicable laws, regulations, and standards.
- Establish requirements for monitoring, detection, and response capabilities.
- Document requirements for supply chain and third-party components.

### 1.2.2 Out of Scope: 
- 

## 2. Stakeholder Map
| Stakeholder Map | Stakeholder | Role / Interest | Influence Level | Contact / Representation | 
|----------|-----------------|-----------------|--------------------------| 
| Internal Security Team | Define and validate security controls | High | | 
| Compliance Officer | Ensure regulatory alignment | High | | 
| End Users | Users of FinApp for intended purposes | Medium | | 
| Third-Party Vendors | Provide integrated services or libraries | Medium | |

## 3. Mission & Ethical Commitments 
- All requirements will directly support policy laid out by the FinApp leadership team.  
- At no time will user data be collected for use other than for the use of the application. Data will only be requested and never gathered without consent. 
- All trade-offs will have an impact identified that takes into account time added to development caused by performance impact to internal teams, and CIA impact to end users. Weighting will be given at 40% for time added to 60% for CIA impact. CIA impact will be translated into a time estimate such that it recognizes the time a user will spend remediating issues, or requesting fixes. 
 

## 4. Assumptions 
For development and release of FinApp, it is assumed that:
- GitHub will be the primary code repository, with the main branch matching the latest release version
- For prototypes 
    - Languages will identified as any secure and mature language the contributor is proficient in. Prototypes must be able to pass integration tests, unit tests, code quality checks, secret scanning tests, 
    - Databases will identified as compatible with the prototyping language will be used. Databases must be able to pass integration tests, and must be able to be secured to follow the current integration testing complexity. 
- For releases :
    - Languages will include requirements from prototyping languages as well as be restricted to performant, memory safe languages. These will include C#, JavaScript, Go and Rust.
    - Databases will be mature, open-source, and secure. These will include PostGreSQL.
- Contributors must have access to MFA-capable devices. 

## 5. Constraints 
- There is no budget for acquiring resources in development or deployment of this project. 

## 6. Trade Offs
| Decision Area | Option Chosen | Rationale | Impact | 
|--------------|-----------|--------| 
| Encryption Strength vs. Performance | AES-256 | Meets compliance, acceptable latency | Slight CPU overhead |
| Development speed vs. Issue remediation | Issue remediation | Focus must be on protecting users and contributors | Slower development of initial product and future enhancements | 


## 7. Applicable Laws, Regulations, and Standards 
| Category | Regulation / Standard | Applicability | 
|----------|-----------------------|---------------|
| Internal Policy | NIST based<br>Adapted for small project work | Mandatory | 
| Financial | SOX, PCAOB | Advisory | U.S. market | 
| Security | NIST 800-53 | Advisory | Align with internal standards | 
| Privacy | GDPR, CCPA | Advisory | Data handling and consent |  

## 8. Risk Tolerance & Initial Assessment 
See [Initial Organization Risk Assessment](../Concepts\ and\ Assessment/Initiation\ Orginizational\ Risk\ Assessment.md)
Risk Appetite Statement: Based on the initial risk assessment, the project will not accept risk that increases the time to recover by more than 12 hours. This will ensure that contributors are unencumbered by low criticality remediation, but users will be protected from vulnerabilities that directly conflict with project goals. 

## 9. Monitoring, Detection, and Response Requirements 
- All monitoring will be done with logging to begin with. This means that all actions performed by prototypes, releases, tests, and security systems must provide detailed event logs. Logging message format is covered in [Central Logging Format](../../Governance/Procedures/Central\ Logging\ Format.md)
- Log reviews will be done daily to look for issues in third party artifacts or build pipeline issues. 
- Responses will be done on a per-availability bases. When a contributor is able to attend to an open issue, this will be worked on before further development is done.

## 10. Supply Chain & Third-Party Requirements 
- All third-party artifacts must have a risk assessment done. Criteria for passing will be based on artifact maturity, community support, and vulnerabilities' time to remediate within the past year. An artifact will not be used if it fails two of the following portions of the assessment:
    - The artifact was release less than 6 months prior to the assessment
    - There is no official community support
    - Vulnerabilities take longer than 1 month to patch
- A complete and up-to-date list of all artifacts must be kept visible on the top-level ReadMe.md at all times
- Vulnerabilities discovered in third-party artifacts must be documented within 3 days as an issue. 

## 11. Traceability & Version Control 
- All requirements will be tagged with unique IDs. Naming convention format is covered in [Naming Conventions](../../Governance/Procedures/Naming\ Conventions.md) 
- Changes logged in Git messages must contain the following:
    - A concise subject line with written in an imperative mood
    - A body that explains why the change was done, what problem or issue it solved, how it was done, and the issue number it addresses, if applicable. 
    - Git messages should be consistently worded and formatted according to each contributors preferred style and lexicon.

