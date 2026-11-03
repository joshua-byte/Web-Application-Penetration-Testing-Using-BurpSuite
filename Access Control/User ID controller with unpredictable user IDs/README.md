# User ID Controlled by Request Parameter, with Unpredictable User IDs

**Platform:** PortSwigger Web Security Academy  
**Tool:** Web Browser  
**Status:** Completed

## Objective
Exploit an IDOR vulnerability to access another user's account information using an unpredictable user ID.

## Methodology
- Logged in using the provided test account.
- Inspected application URLs and identified the user ID parameter.
- Obtained Carlos's user ID from another location in the application.
- Replaced the original user ID with Carlos's identifier.
- Accessed Carlos's account information and retrieved his API key.

## Result
Successfully accessed another user's account information, demonstrating horizontal privilege escalation.

## Vulnerability Details
- **Vulnerability:** Insecure Direct Object Reference (IDOR)
- **CWE:** CWE-639 — Authorization Bypass Through User-Controlled Key
- **CVSS v3.1:** 4.3 — Medium (indicative)

## Key Concepts
- Broken access control
- Horizontal privilege escalation
- IDOR
- Unpredictable identifiers
- Server-side authorization

**Disclaimer:** Conducted in an authorised PortSwigger Web Security Academy lab environment.
