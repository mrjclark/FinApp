---
policy_ID: "P17"
title: "AI Use Policy"
status: "Approved"                # Options: Draft, Approved, Deprecated
document_owner: "mrjclark"
document_maintainer: "mrjclark"
last_approved: "20250810"
next_review: "20260810"
---
# AI Use Policy

## 1. Purpose & Scope

### 1.1 Purpose
To define the principles and requirements for the responsible use of Artificial Intelligence (AI) in the FinApp project, in alignment with NIST’s AI Risk Management Framework (AI RMF 1.0) and related publications (e.g., NIST AI 100-5, SP 1270).

### 1.2 Scope
This policy applies to all interactions with AI systems, including Large Language Models (LLMs) and other AI tools, in the context of the FinApp project.  
Note: At this time, AI LLMs are only consulted to assist in project development (e.g., code suggestions, documentation, design). No AI or machine learning capabilities are used within the FinApp application itself.

## 2. Policy Statement
The FinApp project is committed to ensuring the ethical, secure, and responsible use of AI, aligning with NIST’s AI Risk Management Framework (AI RMF 1.0) and related publications (e.g., NIST AI 100-5, SP 1270). All AI systems or tools consulted during development must be used with transparency and integrity, with a clear distinction between tool-assisted development and application functionality.

## 3. Policy Objectives
- Ensure transparency and documentation of all AI use in development.
- Promote ethical use of AI, respecting privacy, copyright, and legal standards.
- Prevent sharing of sensitive or personal data with external AI systems or LLMs.
- Require human oversight and approval of all AI-assisted outputs before integration.
- Prohibit embedded AI or machine learning features in the application unless a risk assessment is completed.
- Conduct risk assessments prior to any future AI integration, considering security, bias, reliability, and compliance.

## 4. Roles & Responsibilities

| Role                  | Responsibilities                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AI Use Policy Steward     | Maintain and update the AI Use Policy in alignment with NIST guidance. Ensure AI is used only for development suggestions, not embedded in production.     |
| AI Risk Gatekeeper        | Evaluate risks of AI-generated outputs before production use. Review for bias, reliability, and explainability. Maintain audit-ready decision logs.         |
| Human Review Lead         | Oversee manual validation of all AI-generated suggestions. Ensure human approval precedes any implementation. Maintain traceability of decisions.           |
| AI Standards Liaison      | Track evolving AI standards (e.g., NIST AI RMF, AI 100-5). Advise team on trustworthy AI practices. Coordinate with external stakeholders as needed.        |
| Bias and Ethics Reviewer  | Apply SP 1270 principles to assess socio-technical risks. Flag bias or ethical concerns in AI-assisted suggestions. Participate in review sessions.         |



## 5. AI Use Activities

### 5.1 Risk Management
- Establish an AI governance structure aligned with organizational values and risk tolerance.
- Document AI use cases, limitations, and human oversight requirements.
- Define procedures for risk identification, measurement, and mitigation across the AI lifecycle.
- Ensure transparency and accountability in AI-assisted development.
- Maintain traceability between AI-generated suggestions and final implementation decisions.

### 5.2 Global Engagement on AI Standards
- Adopt international AI standards that promote safety, transparency, and interoperability.
- Participate in multistakeholder dialogues on AI governance.
- Align internal policies with U.S. and global AI standardization efforts.
- Promote responsible AI use through documentation and public engagement.
- Avoid premature deployment of AI without conformity assessments.

### 5.3 Managing Bias in AI
- Implement human-in-the-loop review processes to mitigate bias.
- Assess socio-technical risks, including systemic and institutional bias.
- Document datasets, assumptions, and model limitations.
- Apply participatory design and stakeholder input to AI-assisted workflows.
- Avoid embedding AI outputs without fairness and reliability validation.

## 6. Exceptions
There will be no exceptions to policies. Policies will be upheld by all project members at all times.

## 7. Review & Maintenance
* Reviewed annually or upon significant changes.

## 8. References
- [NIST AI RMF 1.0](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST AI 100-5](https://www.nist.gov/publications/nist-ai-100-5)
- [NIST SP 1270](https://www.nist.gov/publications/nist-sp-1270)

---

## Appendix

### A. Definitions
| Term | Definition |
|------|------------|
| Artificial Intelligence (AI) | Systems that perform tasks normally requiring human intelligence, such as reasoning, learning, and decision-making. |
| Large Language Model (LLM)   | AI models trained on large datasets to generate human-like text and assist with development


### B. Version History
Version history tracked via Git commit log.

