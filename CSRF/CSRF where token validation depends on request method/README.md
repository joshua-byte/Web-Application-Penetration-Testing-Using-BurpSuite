# CSRF Where Token Validation Depends on Request Method
## Objective
Test whether CSRF token validation is applied consistently when the email-change function is requested using different HTTP methods.

## Methodology
1. Inspected the account email-change function while signed in to the lab.
2. Intercepted the request using Burp Suite.
3. Sent a POST request without the CSRF parameter and observed that it was rejected.
4. Changed the request method to GET and observed that the response requested the email parameter rather than a CSRF token.
5. Created an HTML form that submitted the email-change request using GET.
6. Stored and delivered the proof-of-concept through the lab exploit server.
7. Confirmed successful lab completion.

## Recommendations
- Apply CSRF protection consistently to all state-changing operations.
- Do not use GET requests to change application data.
- Validate CSRF tokens server-side for every relevant state-changing request.
- Use `SameSite` cookie settings as an additional defence.

