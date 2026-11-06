# DOM-Based XSS

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Lab:** DOM XSS in `document.write` sink using source `location.search`
- **Difficulty:** Apprentice
- **Status:** Completed

## Description
Identified and exploited a DOM-based Cross-Site Scripting vulnerability through the application's search functionality.

## Source and Sink
- **Source:** `window.location.search`
- **Processing:** `URLSearchParams`
- **Sink:** `document.write()`

## Tools Used
- Burp Suite
- Web Browser

## Remediation
- Avoid using `document.write()` with untrusted input.
- Use safe DOM methods such as `textContent`.
- Validate and safely handle URL parameters.
