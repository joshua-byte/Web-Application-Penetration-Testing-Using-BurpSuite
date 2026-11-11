# API Testing – Burp Suite Labs

This section documents two completed API security labs from PortSwigger Web Security Academy. Testing was performed with Burp Suite Community Edition in authorized training environments.

## Key Learning Points

- API documentation can reveal routes and operations that are not obvious in the user interface.
- API endpoints should enforce authorization on the server for every sensitive operation.
- Endpoints not linked from the interface may still be callable directly.
- Sensitive business values, such as product prices, must be controlled and validated by the server.
- Request formats and content types can affect how an API processes input, but a successful request must still be checked against business rules and user permissions.

