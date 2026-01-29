# IDOR Practice

## Lab
PortSwigger Web Security Academy

## What I tested
Object-level authorization handling.

## Result
By changing the object ID in the request, it was possible to access data belonging to another user.

## Lesson Learned
Authorization must be enforced on the server side for every request.
