# Reflected XSS – Practice Lab

## Lab Platform
PortSwigger Web Security Academy / PentesterLab

## Description
During testing of user input reflection, I found that the application reflects input directly in the response without proper output encoding.

## Testing Process
- Located a search parameter reflected in the response
- Injected a simple JavaScript payload
- Verified script execution in the browser
- Confirmed the payload was reflected without sanitization

## Impact
An attacker could execute arbitrary JavaScript in the victim’s browser, potentially leading to session theft or user redirection.

## Mitigation
User input should be properly encoded based on context, and a strong Content Security Policy (CSP) should be implemented.
