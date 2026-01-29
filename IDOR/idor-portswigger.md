# IDOR – PortSwigger Lab

## Lab Platform
PortSwigger Web Security Academy

## Description
While testing object-level access control, I noticed that the application relies on user-supplied identifiers without properly verifying ownership on the server side.

## Testing Process
- Logged in as a normal user
- Intercepted requests using Burp Suite
- Identified an object ID parameter in the request
- Modified the ID to reference another user’s resource
- The server returned data that did not belong to my account

## Impact
This issue allows unauthorized access to other users’ data, which can lead to privacy violations and data exposure.

## Mitigation
All object access should be validated on the server side by checking resource ownership, regardless of the user’s role or request source.
