# JWT Authentication Bypass via Unverified Signature

## Objective

Test whether the application verifies the signature of a JWT before trusting its contents.

## Methodology

1. Logged in to the application and inspected the requests in Burp Suite.
2. Identified the JWT being sent with authenticated requests.
3. Inspected the JWT header and payload using Burp Suite's JSON Web Token view.
4. Changed the `sub` claim from `wiener` to `administrator`.
5. Sent a request using the modified token.
6. Accessed the administrative functionality and sent the request to delete the `carlos` user.

## Recommendations

- Always verify JWT signatures on the server.
- Use a secure, explicitly configured signing algorithm.
- Validate claims such as issuer, audience and expiration.
- Enforce authorization checks for administrative actions.

