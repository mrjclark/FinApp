# Information Security Standards

## 1. Purpose

This standard defines the minimum security requirements for access control, authentication, and encryption to protect sensitive information within the organization’s systems and data.

## 2. Scope

These standards apply to all systems, applications, and personnel handling or accessing sensitive data within the organization.

---

## 3. Access Control Implementation

### 3.1 Principle of Least Privilege
- Users, processes, and devices shall be granted the minimum access necessary to perform their job functions.
- Access reviews must be conducted at least yearly.

### 3.2 Role-Based Access Control (RBAC)
- Define and maintain roles with specific permissions.
- Assign users to roles based on job responsibilities.
- Document all roles and associated permissions.

### 3.3 Access Requests and Approvals
- All access requests must be formally submitted and approved by the project owner.
- Maintain records of all access requests, approvals, and removals.

### 3.4 Access Revocation
- Access must be immediately revoked upon termination or role change.
- Automated processes for account de-provisioning must be implemented.

---

## 4. Secure Authentication Requirements

### 4.1 Multi-Factor Authentication (MFA)
- MFA must be enabled for all privileged and remote access accounts.
- At least two factors (something you know, have, or are) must be used.

### 4.2 User Password Policy
- Minimum password length: 12 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 5 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).

### 4.3 Privileged User Password Policy
- Privileged accounts are defined those which have direct access to change source code in the project.
- Minimum password length: 24 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 10 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).


### 4.4 System Account Password Policy
- System accounts are used for system to system communication only.
- System accounts shall not be used to interactively access project resources through human operation.
- Minimum password length: 24 characters.
- Require a mix of uppercase, lowercase, numeric, and special characters.
- Prohibit reuse of the last 10 passwords.
- Passwords must be stored using strong, salted hashing algorithms (e.g., bcrypt, Argon2).

### 4.3 Session Management
- Invalidate sessions after password changes or account lockout.

### 4.4 Account Lockout
- Lock accounts after 5 failed login attempts within 10 minutes.
- Locked accounts can be unlocked only by an administrator or through secure self-service.

---

## 5. Encryption Standards

### 5.1 Data at Rest
- All sensitive data must be encrypted at rest using industry-standard algorithms (e.g., AES-256).
- Encryption keys must be managed securely, with access restricted to authorized personnel only.
- Regularly rotate encryption keys and audit key usage.

### 5.2 Data in Transit
- All data transmitted over public or untrusted networks must use TLS 1.2 or higher.
- Disable insecure protocols (e.g., SSL, TLS 1.0/1.1).
- Validate certificates and reject expired or self-signed certificates in production systems.

---

## 6. Compliance and Monitoring

- Regularly audit access control, authentication, and encryption configurations.
- Document and remediate any deviations from these standards.
- Provide training to ensure personnel understand and follow these requirements.

---

## 7. Exceptions

Any exceptions to this standard must be formally documented, risk-assessed, and approved by the Information Security Officer.

---

## 8. Review

This standard shall be reviewed at least annually or upon significant changes to relevant technology or regulations.

---

**Document Owner:**  mrjclark
**Approval Date:**  20250627
**Next Review Date:**  20260627
