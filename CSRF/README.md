# Cross-Site Request Forgery (CSRF)


## What is CSRF?

Cross-Site Request Forgery (CSRF) is a web application vulnerability that allows an attacker to induce an authenticated user's browser to perform unintended actions on a website.

## How CSRF Works

1. A user logs in to a web application.
2. The application stores an authentication session, commonly through a cookie.
3. The user visits a malicious or attacker-controlled webpage while still authenticated.
4. The webpage causes the browser to send a request to the target application.
5. If the application lacks effective CSRF protections, it may process the request using the user's authenticated session.

## Common Attack Scenarios

Depending on the application's functionality, CSRF may be used to:

- Change account email addresses or profile information.
- Modify account security settings.
- Create or modify application data.
- Perform actions using the victim's authenticated session.
- Initiate transactions or other sensitive operations.

## Testing Methodology

1. Identify authenticated functions that modify application state.
2. Inspect the relevant HTTP requests using Burp Suite.
3. Check for CSRF tokens and other request-validation mechanisms.
4. Determine whether the request can be submitted cross-site.
5. Construct a proof-of-concept HTML page in an authorised testing environment.
6. Verify whether the action succeeds using a controlled test account.
7. Document the request, response, impact and available security protections.

## Common CSRF Defences

### 1. CSRF Tokens
Use unpredictable, session-bound tokens and validate them on the server for every state-changing request.

### 2. SameSite Cookies
Configure session cookies with an appropriate `SameSite` attribute, such as `Lax` or `Strict`, where compatible with application requirements.

### 3. Origin and Referer Validation
Validate the `Origin` header for state-changing requests. `Referer` validation can be used as a carefully implemented fallback.

### 4. Re-authentication
Require additional authentication or confirmation for sensitive operations, such as changing account recovery details.

### 5. HTTP Method Restrictions
Do not use GET requests for state-changing operations. Use appropriate HTTP methods alongside server-side CSRF protections.
