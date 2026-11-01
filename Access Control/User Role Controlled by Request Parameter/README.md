# User Role Controlled by Request Parameter

**Platform:** PortSwigger Web Security Academy  
**Tool:** Burp Suite Community Edition, Browser Developer Tools  
**Status:** Completed

## Objective
Exploit improper access control by manipulating a client-controlled cookie to gain administrative privileges.

## Methodology
- Logged in using the regular `wiener` account.
- Inspected browser cookies and identified the `Admin` cookie.
- Changed its value from `false` to `true`.
- Accessed the administrative panel.
- Deleted the `carlos` account to complete the lab.

## Result
Successfully performed vertical privilege escalation and gained administrative access.

## Vulnerability Details
- **Vulnerability:** Broken Access Control
- **CWE:** CWE-639 — Authorization Bypass Through User-Controlled Key
- **CVSS v3.1:** 8.1 — High (indicative)

## Key Concepts
- Cookie manipulation
- Vertical privilege escalation
- Client-side trust
- Server-side authorization
