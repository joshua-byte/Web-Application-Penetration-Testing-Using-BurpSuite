# 2FA Simple Bypass

**Platform:** PortSwigger Web Security Academy  
**Tool:** Web Browser  
**Status:** Completed

## Objective
Exploit a weakness in the two-factor authentication process to access another user's account without completing the intended verification.

## Methodology
- Accessed the two-factor authentication flow.
- Examined the security-code email.
- Modified the account identifier in the account URL.
- Accessed the target account without completing the expected 2FA verification.

## Result
Successfully bypassed the 2FA mechanism and accessed the `carlos` account in the lab environment.

## Key Concepts
- Two-factor authentication bypass
- Broken access control
- Authentication flow manipulation
