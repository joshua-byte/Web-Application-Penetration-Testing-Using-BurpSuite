# Password Reset Broken Logic

**Platform:** PortSwigger Web Security Academy  
**Tool:** Burp Suite Community Edition  
**Status:** Completed

## Objective
Exploit a weakness in the password-reset mechanism to change another user's password.

## Methodology
- Initiated a password-reset request for the `wiener` account.
- Intercepted the request using Burp Suite.
- Modified the `username` parameter from `wiener` to `carlos`.
- Submitted the modified request using the reset token.
- Successfully changed the target account's password.

## Result
Successfully exploited the password-reset logic and gained access to the `carlos` account.

## Vulnerability Details
- **Vulnerability:** Broken Password Reset Logic
- **CWE:** CWE-640 — Weak Password Recovery Mechanism
- **CVSS v3.1:** 9.1 — Critical (indicative)

## Key Concepts
- Password reset vulnerabilities
- Reset-token validation
- Account takeover
- Broken authentication logic
