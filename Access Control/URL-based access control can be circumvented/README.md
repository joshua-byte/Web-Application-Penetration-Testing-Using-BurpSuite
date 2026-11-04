# URL-Based Access Control Can Be Circumvented

**Platform:** PortSwigger Web Security Academy  
**Difficulty:** Apprentice  
**Category:** Access Control  
**Tool:** Burp Suite  
**Status:** Completed

## Objective
To bypass URL-based access restrictions and gain access to administrative functionality.

## Methodology
1. Attempted to access `/admin` directly and received an `Access denied` response.
2. Intercepted the request using Burp Suite.
3. Added the `X-Original-Url: /admin` header while requesting `/`.
4. Successfully accessed the administrative panel.
5. Used `X-Original-Url: /admin/delete` with the `username=carlos` parameter to trigger the account deletion.

## Result
Successfully bypassed the access restriction, accessed the admin panel, and deleted the Carlos account. The lab was solved.

## Vulnerability Details
- **Vulnerability:** Broken Access Control
- **Technique:** URL-based access-control bypass
- **CWE:** CWE-863 – Incorrect Authorization (indicative classification)
- **Impact:** Unauthorized access to administrative functionality and account deletion.
