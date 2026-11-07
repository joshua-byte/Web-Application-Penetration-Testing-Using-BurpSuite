# Reflected XSS - HTML Attribute

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Lab:** Reflected XSS into attribute with angle brackets HTML-encoded

## Description
Identified and exploited a reflected XSS vulnerability by injecting an event handler into a quoted HTML attribute.

## Payload
```html
"onmouseover="alert(1)
```
## Tools Used
- Burp Suite
- Web Browser

## Remediation
- Implement context-sensitive output encoding.
- Safely handle quotation marks in HTML attributes.
- Avoid unsafe handling of user-controlled input.
