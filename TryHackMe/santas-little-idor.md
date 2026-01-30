# Santa’s Little IDOR – TryHackMe

## Room Difficulty
Medium

## Overview
This room demonstrates an Insecure Direct Object Reference (IDOR) vulnerability caused by improper server-side authorization checks on object identifiers.

The main focus of the lab is understanding how object IDs are generated, exposed, and validated by the application, and how manipulating those identifiers can lead to unauthorized data access.

## Environment Setup
- The target machine was deployed on TryHackMe
- A VPN connection was established from Kali Linux to gain access to the lab environment
- Traffic analysis was performed using standard interception techniques

## Vulnerability Analysis
The application uses object identifiers to reference user-related resources. These identifiers are exposed in requests and can be user-controlled.

During testing, different ID formats were analyzed, including:
- UUIDs
- Encoded identifiers (e.g., Base64)
- Hashed identifiers (e.g., MD5)

Understanding the ID format is important to determine whether it can be predicted, decoded, or modified during testing.

## Testing Methodology
- Intercepted HTTP requests containing object identifiers
- Identified parameters referencing user-specific resources
- Modified the object ID values in the request
- Observed that the server did not properly verify object ownership
- Successfully accessed data belonging to other users

## Impact
This vulnerability allows unauthorized access to sensitive user data and represents a clear access control failure. If exploited in a real-world application, it could lead to data leakage and privacy violations.

## Mitigation
- Enforce strict server-side authorization checks for every object access
- Do not rely on obscurity or encoding of object identifiers
- Ensure that object ownership is validated independently of user input
