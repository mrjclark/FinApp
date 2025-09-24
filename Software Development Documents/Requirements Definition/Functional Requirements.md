---
title: "Requirements for Initial Development"
status: "Draft"
version: "0.1"
author: "mrjclark"
date_created: "20250912"
last_updated: "20250912"
tags:
  - @requirements
contributor_roles:
  - "Contributors"
---

# Requirements for Initial Development

## 1. Purpose and Scope

### 1.1 Purpose
This document will cover all features that must be present for the first release of FinApp

### 1.2 Scope
This will cover the first all requirements up to the first release of FinApp

## 2. Functional Requirements

### 2.1 Database requirements

#### 2.1.1 Setup
An initial script must be available to setup the database according to the system. This should be written for both SQLite and PostgreSQL.
Encryption must be setup on the database as a first step.

#### 2.1.2 Tablespaces
One table space will be for user, financial data
One table space will be for all other metadata
One table space will be for calculated data

#### 2.1.3 Users
During development, there will be one user that allows for interactive login. This will be removed when deploying for release.
Other users to include are:
- One user per CRUD action per table. New users will be created when tables are created. 
- One user for DDL create operations. Users for DDL update and delete will be created when a new object is created.

#### 2.1.4 Tables
master_Findata - Stores a list of all financial transactions input by the user
master_Metadata - Stores a list of all financial institutions and related columns outside of what is covered in the master_Findata table
master_Calcdata - Stores a list of the calculated data tables
adhoc_Findata - An initial table created so that users can input financial transaction data without first needing to set up institutions
currency_Metadata - Stores a list of currencies for conversion.

#### 2.1.5 Columns, Keys, Indexes, Triggers
All tables will use a unique ID for each row for relations to other tables. One master financial data table will be kept that has a normalized record of all financial transactions. There will be one master meta data table to have a list of all created tables from creation of financial institutions. There will be one master calculated table that has a list of all calculated data tables. Tables will be created using specifications stored in the master meta or calculated tables. All tables will have triggers before insert or update for validating incoming data. All tables will have triggers after insert, update, or delete for auditing changes. Define each table using the following format.

| Table Name | Object | Object Name | Specification 1 | Specification 2 | Specification 3 | Specification 4 |

#### 2.1.6 Procedures
Database maintenance procedures will be needed to minimize the database size and stabalize performance. 

#### 2.1.7 Functions
Functions will be needed for currency conversion.

#### 2.1.8 Views
Depending on database and table sizes, materialzied views need to be created to ensure performance does not reduce data viewing speeds

#### 2.1.9 Encryption
All data in tables must be encrypted per project standards

#### 2.1.10 Secret Management
All passwords must be rotated automatically. 

### 2.2 Backend Engine Requirements

#### 2.2.1 Authentication & Authorization
There should be role-based access controls (RBAC) across all endpoints.There should be short-lived tokens (e.g. JWT with refresh logic) and validate scopes per action. If any federated access is needed, integrate with identity providers.

#### 2.2.2 Secret Management
Secrets will never be stored in plain text, environment variables, or in unsecured locations. Secrets will be periodically rotated and log access events. Ensure secrets are only accessible to the minimal set of services that require them.

#### 2.2.3 Data Encryption
Encrypt data at rest using database-native encryption (e.g. TDE for SQL, KMS-integrated for NoSQL). Encrypt data in transit using TLS 1.2+ with mutual authentication if needed. For sensitive fields (e.g. PII, credentials), consider field-level encryption with key separation.

#### 2.2.4 Audit & Traceability
Every backend action will be logged with timestamp, actor, and intent. Include correlation IDs across UI, backend, and database layers for traceable workflows. Store logs in tamper-evident systems and rotate them securely.

#### 2.2.5 Input Validation & Sanitization
Validate all incoming data against strict schemas (e.g. JSON Schema, Protobuf). Sanitize inputs to prevent injection attacks—especially for database queries and secret access.

#### 2.2.6 Rate Limiting & Throttling
Apply per-user rate limits to backend endpoints. Use circuit breakers and backpressure mechanisms to prevent overload and abuse.

#### 2.2.7 Error Handling & Redaction
Ensure error messages never leak sensitive data (e.g. stack traces, query fragments). Use symbolic error codes and map them to user-friendly messages at the UI layer. The application needs to fail in a safe state. Crashes should ensure all open or orphaned connections are closed.

#### 2.2.8 Secure Data Access Patterns
Use parameterized queries or ORM with strict query builders. Avoid dynamic query construction unless fully sanitized. Implement read/write separation and least privilege for database roles. 

#### 2.2.9 Dependency & Package Hygiene
Pin versions of backend libraries and scan for vulnerabilities (e.g. Snyk, OWASP Dependency-Check). Isolate backend services in containers with minimal base images.

### 2.2.10 Resilience & Recovery
Design for graceful degradation—fallbacks for secret access, cached reads for DB failures. 
