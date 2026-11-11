# Access Control – Unprotected Admin Functionality

## Overview

This assessment covered two PortSwigger labs involving unprotected administrative functionality. The objective was to discover hidden administrative URLs, access the admin panel as a regular user and perform an unauthorized administrative action.

## Objective

Identify exposed administrative functionality and demonstrate how insufficient access restrictions can allow unauthorized users to access administrative features.

## Methodology

1. Opened the target application and inspected the homepage and available functionality.
2. Examined the application's publicly accessible resources and HTTP responses to identify references to administrative functionality.
3. Inspected `robots.txt` and discovered an administrative path that was not linked through normal application navigation.
4. Used Burp Suite to intercept the homepage request and examine the server response, including its JavaScript code.
5. Identified another administrative URL referenced in the client-side JavaScript.
6. Accessed the discovered administrative URLs directly through the browser.
7. Confirmed that the administrative panels were accessible without proper authorization.
8. Located the user management functionality and used the delete option to remove the `carlos` account.
9. Verified that the application displayed a successful deletion message and that the lab was marked as solved.

## Security Impact

An unauthorized user could access administrative features and perform actions intended only for administrators. Depending on the functionality exposed, this could result in account deletion, unauthorized changes or other administrative actions.

## Recommendations

- Enforce server-side authorization checks on all administrative pages and actions.
- Do not rely on hidden or unpredictable URLs to protect sensitive functionality.
- Avoid exposing unnecessary internal paths in publicly accessible files and client-side code.
- Restrict administrative operations to properly authorized users.
- Verify permissions on every sensitive request, not just when displaying the page.
