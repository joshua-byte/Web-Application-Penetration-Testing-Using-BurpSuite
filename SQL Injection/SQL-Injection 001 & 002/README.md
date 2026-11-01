# SQL Injection 001 & 002

## Labs Completed

### 1. SQL Injection — Hidden Data Retrieval

- **Vulnerable parameter:** `category`
- **Objective:** Retrieve hidden product records by manipulating the application's SQL query.
- **Payload:**
  ```sql
  ' OR 1=1-- -
  ```
- **CVSS v3.1:** 5.3 — Medium (indicative)
- **Status:** Solved

### 2. SQL Injection — Authentication Bypass

- **Vulnerable parameter:** `username`
- **Objective:** Bypass the application's authentication mechanism and access the administrator account.
- **Payload:**
  ```sql
  administrator'--
  ```
- **CVSS v3.1:** 9.1 — Critical (indicative)
- **Status:** Solved


## Documentation

A detailed penetration-testing report accompanies these exercises, covering technical analysis, exploitation evidence, CVSS scoring, MITRE ATT&CK mapping, and remediation recommendations.
