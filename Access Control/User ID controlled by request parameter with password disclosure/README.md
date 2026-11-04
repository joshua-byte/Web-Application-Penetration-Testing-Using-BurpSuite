# User ID Controlled by Request Parameter with Password Disclosure

**Platform:** PortSwigger Web Security Academy  
**Tools:** Browser Developer Tools  
**Status:** Completed

## Objective
Exploit broken access control to access an administrator's account and identify exposed credentials.

## Methodology
- Logged in using the regular `wiener` account.
- Manipulated the user ID parameter to access the administrator's account page.
- Inspected the HTML using browser developer tools.
- Discovered the administrator's password in the password input's `value` attribute.
- Used the exposed credentials to access the administrator account.
- Accessed the admin panel and deleted the `wiener` account.

## Result
Successfully gained administrative access through IDOR and sensitive password disclosure.

## Vulnerability Details
- **Vulnerabilities:** Broken Access Control and Sensitive Information Disclosure
- **CWE:** CWE-639 — Authorization Bypass Through User-Controlled Key
- **CVSS v3.1:** 8.3 — High (indicative)

## Key Concepts
- IDOR
- Horizontal and vertical privilege escalation
- Password disclosure
- HTML inspection
- Server-side authorization

**Disclaimer:** Conducted in an authorised PortSwigger Web Security Academy lab environment.
