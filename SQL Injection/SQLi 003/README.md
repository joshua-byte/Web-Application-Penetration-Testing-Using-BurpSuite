# SQL Injection — UNION Attack

Lab: SQL injection UNION attack, retrieving multiple values in a single column

**Platform:** PortSwigger Web Security Academy  
**Tool:** Burp Suite Community Edition  
**Status:** Completed

## Objective

Exploit a UNION-based SQL injection vulnerability to retrieve multiple values from a database through a single column.

## Methodology

- Identified a text-compatible column using `UNION SELECT`.
- Used string concatenation (`||`) to combine multiple database fields.
- Used a delimiter (`~`) to distinguish retrieved values.
- Retrieved usernames and passwords from the users table.

## Key Concepts

- UNION-based SQL injection
- Column enumeration and data-type compatibility
- SQL string concatenation
- Database information disclosure

## Classification

- **CWE:** CWE-89 — SQL Injection
- **MITRE ATT&CK:** T1190 — Exploit Public-Facing Application
- **CVSS v3.1:** 8.2 — High (indicative assessment)
