# Reflected XSS

**Platform:** PortSwigger Web Security Academy

**Lab:** Reflected XSS into HTML context with nothing encoded

**Difficulty:** Apprentice

## Description
Identified and exploited a reflected Cross-Site Scripting (XSS) vulnerability through the application's search functionality.

## Payload
```html
<script>alert(1)</script>
```

## Tools Used
- Burp Suite
- Web Browser

## Result
Successfully executed JavaScript in the browser and solved the lab.

## Remediation
- Implement context-aware output encoding.
- Validate and sanitise untrusted input where appropriate.
- Avoid unsafe HTML insertion methods.
