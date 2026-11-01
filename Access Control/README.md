# Access Control Vulnerabilities

Hands-on access control assessments conducted through **PortSwigger Web Security Academy**, using **Burp Suite Community Edition** and browser developer tools.

## Labs Completed

### 1. User Role Controlled by Request Parameter
- **Objective:** Gain administrative access by manipulating a client-controlled role parameter.
- **Method:** Changed the `Admin` cookie value from `false` to `true`.
- **Result:** Accessed the admin panel and successfully deleted the `carlos` account.
- **CVSS v3.1:** 8.1 — High (indicative)
- **Status:** Completed

## Key Concepts
- Broken access control
- Vertical privilege escalation
- Cookie manipulation
- Server-side authorization

## Tools Used
- Burp Suite Community Edition
- Browser Developer Tools

**Disclaimer:** All testing was conducted in authorised PortSwigger Web Security Academy lab environments.
