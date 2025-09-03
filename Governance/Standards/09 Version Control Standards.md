---
standard_ID: "S09"
title: "Version Control Standards"
status: Draft
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approval: "20250903"
next_review: "20260902"
---

# Version Control Standards

## 1. Purpose & Scope

### 1.1 Purpose
This standard defines the minimum requirements for secure, auditable, and contributor-friendly version control practices within FinApp. It supports traceability, integrity, and stewardship across the software development lifecycle, aligning with NIST and OWASP guidance.

### 1.2 Scope
Applies to all FinApp source code, configuration files, and infrastructure-as-code artifacts managed in version control systems (e.g., Git). All contributors, maintainers, and automation systems interacting with repositories are subject to this standard.

### 2. Roles & Responsibilities

| Role | Responsibilities |
|------|------------------|
| Owner | Establishes and enforces the standard. Reviews and approves exceptions. |
| Contributors | Implements tasks aligned to the standard. Escalates deviations. |
| Maintainers | Enforces branch protections, reviews pull requests, and ensures audit traceability. |

## 3. Standard Requirements

### 3.1 Repository Management
- All source code must reside in a version-controlled repository.
- Repositories must enforce branch protections and require pull request reviews.
- Production branches must be tagged and documented upon merge.

### 3.2 Commit Hygiene
- Commits must be signed and traceable to individual contributors.
- Commit messages must include purpose and relevant control IDs.
- No direct commits to protected branches.

### 3.3 Audit & Traceability
- Version control logs must be retained for at least 12 months.
- All merges to production must be tagged and linked to change records.
- Contributors may be asked to attest via signed commits or onboarding checklists.

## 4. Implementation Guidance
- Use GitHub/GitLab branch protection rules and CODEOWNERS files.
- Integrate SAST tools (e.g., Semgrep, CodeQL) into CI pipelines.
- Use GPG or SSH keys for commit signing.
- Maintain an onboarding checklist with control IDs.

## 5. Exceptions
- Exceptions must be documented, risk-assessed, and approved.
- Reviewed at least annually.

## 6. Review & Maintenance
* Reviewed annually or upon significant changes.

## 7. References
- NIST SP 800-218: Secure Software Development Framework (SSDF)
- OWASP Software Supply Chain Security Cheat Sheet

## 8. Audit & Traceability
- Compliance is verified through periodic reviews of implementation artifacts.
- Contributors may be asked to attest to adherence via signed commits or onboarding checklists.

---

Appendix

A. Definitions

| Term | Definition |
|------|------------|
| Signed Commit | A Git commit cryptographically verified to originate from a trusted contributor. |
| Protected Branch | A repository branch with enforced rules (e.g., review required, no direct commits). |

B. Version History
Version history tracked via Git commit log.
