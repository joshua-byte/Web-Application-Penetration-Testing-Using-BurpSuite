# API Testing – Burp Suite Labs

This section documents two completed API security labs from PortSwigger Web Security Academy. Testing was performed with Burp Suite Community Edition in authorized training environments.

## Completed Labs

| Lab | Focus | Status |
|---|---|---|
| [Exploiting an API endpoint using documentation](Exploiting%20an%20API%20endpoint%20using%20documentation/README.md) | Using API documentation to identify and test a user-management operation | Completed |
| [Exploiting an unused API endpoint](Exploiting%20an%20unused%20API%20endpoint/README.md) | Finding an endpoint outside the normal interface and testing product-price handling | Completed |

## Folder Structure

Each lab folder contains:
- `README.md` – lab-specific summary and methodology
- `report.pdf` – formatted report with evidence screenshots
- `report.tex` – editable LaTeX source
- `evidence/` – screenshots supplied for the lab

## Key Learning Points

- API documentation can reveal routes and operations that are not obvious in the user interface.
- API endpoints should enforce authorization on the server for every sensitive operation.
- Endpoints not linked from the interface may still be callable directly.
- Sensitive business values, such as product prices, must be controlled and validated by the server.
- Request formats and content types can affect how an API processes input, but a successful request must still be checked against business rules and user permissions.

## Tools

- Burp Suite Community Edition
- Web browser
- PortSwigger Web Security Academy

**Disclaimer:** All testing was conducted in authorized PortSwigger Web Security Academy lab environments.
