Configuration Management Policy

##1. Purpose and Scope
This policy defines how configuration items are identified, tracked, versioned and changed for FinApp. It ensures consistent, secure and auditable configurations across infrastructure, application code and dependencies.

Scope:
- Applies to all components: source code, infrastructure as code, containers, services and third-party dependencies
- Governs configuration identification, change control, baselining, monitoring and auditing

##2. Roles and Responsibilities
|Role | Responsibility|
|---|---|
|lead developer | maintain configuration baselines, review and approve changes|
|configuration lead | track configuration items, ensure versioning and documentation|
|security auditor | verify compliance with baselines, conduct periodic configuration reviews|
|operations engineer | implement approved changes, maintain automation tools|

##3. Configuration Identification
- maintain an inventory of configuration items (CIs) with unique identifiers  
- categorize CIs by type: infrastructure, application code, container images, libraries  
- define attributes for each CI: version, owner, location, security classification  

##4. Baseline Configuration and Hardening
- establish secure baseline for each CI type (OS, database, container images)  
- document baseline settings and hardening steps (file permissions, service disablement, network settings)  
- store baseline definitions in version control (GitHub repository)

##5. Configuration Change Control
    1. propose change  
       - create issue in GitHub with description, risk assessment, rollback plan  
    2. review and approval  
       - configuration lead and security auditor review proposed changes  
    3. testing  
       - apply change in staging environment and validate against security test suite  
    4. implementation  
       - merge into testing branch, run automated deployment workflows  
    5. documentation  
       - update CI inventory, baseline definitions and changelog  
    6. rollback  
       - if issues arise, execute documented rollback procedure  

##6. Tools and Automation
|Tool | Purpose|
|---|---|
|GitHub | source control, branch protection, audit logs|
|Dockerfile | container build definitions and hardening|
|GitHub Actions | automated change pipelines and tests|

##7. Monitoring and Auditing
- enable audit logs for all configuration changes in source control and infrastructure  
- schedule periodic configuration drift scans (Ansible or other tools)  
- review audit reports quarterly and after major releases  

##8. Exception Management
- document any temporary deviations from baseline in an exceptions register  
- assign an expiry date and risk owner for each exception  
- review and close exceptions when baselines are updated  

##9. Continuous Improvement
- conduct annual policy and baseline reviews to incorporate new security guidance  
- update tools, processes and baselines based on audit findings and emerging threats  
- maintain a backlog of configuration enhancements in GitHub Issues  

---
References
- NIST SSDF (GOV-CM)  
- CIS Control 4: Secure Configuration of Enterprise Assets and Software  
- ISO 27001 / ISO 27002 configuration management controls  
Appendix
- version history:  
  - initial draft – 20250626