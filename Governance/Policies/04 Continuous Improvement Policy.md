---
policy_ID: "P04"
title: "Continuous Improvement Policy"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# Continuous Improvement Policy

## 1. Purpose & Scope

### 1.1 Purpose
To define the commitment and principles for continual improvement of information security for the FinApp project, in accordance with NIST SP 800-137, NIST Cybersecurity Framework 2.0 (CSF), and NIST SP 800-218 Ver 1.1

### 1.2 Scope
This policy applies to all aspects of the FinApp project, including policies, controls, processes, and supporting documentation. All project roles are covered.

## 2. Policy Statement
The FinApp project is committed to ongoing improvement of its information security management system (ISMS). Continual improvement is achieved by monitoring performance, learning from incidents and audits, and implementing corrective and preventive actions. The FinApp project maintains an ISCM strategy to ensure visibility into assets, threats, vulnerabilities, and control effectiveness, in alignment with NIST SP 800-137.

## 3. Policy Objectives
- Regularly review and update information security objectives.
- Identify opportunities for improvement through audits, risk assessments, incident reviews, and feedback.
- Take corrective and preventive actions to address nonconformities and enhance controls.
- Document and track improvements for effectiveness.

## 4. Roles & Responsibilities

| Role | Responsibilities |
|------|------------------|
| Project owner (Security Steward, System Owner) | - Define and uphold governance philosophy and risk posture  <br> - Serve as risk executive and authorizing voice for security decisions <br> - Oversee continuous monitoring and feedback loops <br> - Own mission alignment and system accountability <br> - Ensure secure configuration and lifecycle management <br> - Approve changes and oversee contributor onboarding |
| Contributors (Security Champion, Platform Stewards) | - Advocate secure practices within contributor teams <br> - Support DevSecOps integration and CI/CD hygiene <br> - Lead onboarding for new contributors <br> - Manage infrastructure-as-code and telemetry <br> - Own CI/CD pipelines and secure deployment workflows <br> - Ensure automation supports governance rituals <br> - Follow secure coding and operational practices <br>  - Report issues and support continuous improvement 
| Reviewers (Audit & Compliance Lead) | - Maintain audit traceability and POA&M documentation <br> - Align with NIST controls and other compensating controls <br> - Conduct internal reviews and readiness assessments |
| Third Parties (External Providers, Common Control Providers) | - Deliver services or components under agreed security requirements <br> - Participate in supply chain reviews and maintain inherited controls <br> - Support continuous improvement through feedback and collaboration |

## 5. Continual Improvement Activities

### 5.1 Establish Baselines  
  - Define current cybersecurity posture using maturity models and control assessments  
  
### 5.2 Continuous Monitoring  
  - Maintain visibility into assets, threats, vulnerabilities, and control effectiveness  
  
### 5.3 Governance Integration  
  - Align cybersecurity strategy with enterprise risk management and stakeholder expectations  
  
### 5.4 Feedback Loops  
  - Use telemetry, audit logs, and contributor input to refine controls and workflows  
  
### 5.5 Automation of Controls  
  - Automate assessment, deployment, and remediation workflows  
  
### 5.6 Role Clarity and Accountability  
  - Define and assign roles (e.g., steward, owner, champion) with clear responsibilities  
  
### 5.7 Risk Response and Adaptation  
  - Adjust controls and strategies based on observed risks, incidents, or control failures  
  
### 5.8 Documentation and Traceability  
  - Maintain audit-ready records of changes, assessments, and decisions  
  
### 5.9 Cross-Framework Mapping  
  - Align practices across NIST, OWASP, CIS, and other public frameworks for comprehensive coverage
  
## 6. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 7. Review & Maintenance
* Reviewed annually or upon significant changes.

## 8. References
- [NIST SP 800-137](https://csrc.nist.gov/publications/detail/sp/800-137/final)
- [NIST Cybersecurity Framework 2.0](https://www.nist.gov/cyberframework)
- [NIST SP 800-218 Ver 1.1](https://csrc.nist.gov/publications/detail/sp/800-218/final)

---

## Appendix

### A. Definitions
| Term                      | Definition                                                                 |
|---------------------------|----------------------------------------------------------------------------|
| ISCM                      | Information Security Continuous Monitoring—ongoing awareness of security posture, threats, and control effectiveness. |
| POA&M                     | Plan of Action and Milestones—used to track remediation of identified weaknesses. |
| Configuration Management  | Process for maintaining secure and consistent system configurations. |
| Audit Traceability        | Ability to track decisions, changes, and control assessments for accountability and review. |

### B. Version History
Version history is tracked in the Git commit log.

