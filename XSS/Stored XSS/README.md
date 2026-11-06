# Stored XSS

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Lab:** Stored XSS into HTML context with nothing encoded
- **Difficulty:** Apprentice
- **Status:** Completed

## Description
Identified and exploited a Stored Cross-Site Scripting (XSS) vulnerability through the blog comment functionality.

## Payload
```html
<script>alert(1)</script>
```

## Remediation
- Implement context-sensitive output encoding.
- Use secure HTML sanitisation where necessary.
- Avoid unsafe HTML insertion methods.
