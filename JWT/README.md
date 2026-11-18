# JSON Web Tokens (JWT)

This folder contains notes and practical labs on JSON Web Token (JWT) security, completed through PortSwigger Web Security Academy.

## Common JWT Security Issues

- Accepting tokens without properly verifying their signatures.
- Weak or incorrectly configured signing algorithms.
- Trusting claims that can be changed by the client.
- Failing to validate important claims such as expiry, issuer or audience.
- Using insecure key management.

## Security Testing

When testing JWT authentication:

- Identify where the application sends and stores the token.
- Inspect the header and payload.
- Check how the server responds to modified claims.
- Verify whether the signature and relevant claims are properly validated.
- Confirm that authorization decisions are enforced by the server.

