# Authorization

Authorization is the rights users have. This allows an application to see the differences between users and their roles.

## Table of Contents

- [Explanation](#explanation)
- [Usage](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

**Validate Sessions**
This is very similar to the sessions in authentication, sessions needs to be validated to know who the users is and what their rights within the application are.

**Validate user Role & permissions**
Information on the user and its role is stored in the session. Since this is stored client-side, it is important to make sure that the user cannot change it, this can be done by using a JWT-token. When the entity calls a method the user role is given as a parameter to the backend, it is then compared to the permissions certain users have to see if this current user has the permission to execute the request.

## Usage

The correct implementation should be to validate the session given by the entity when a call is made to make sure the entity has a right to be able to make a call, and the permissions of that entity need to be checked to make sure he has the right to call the specified method.

## Flaws

A flaw that was found in the air quality project was that the session was not checked on roles, only whether it exists or not. This meant that any user that is logged in could access every page, regardless of his role. It is important that all sessions and their roles are validated.

To make sure that the users cannot do too much, it also is important that any given user does not have too many rights. If it does not needs to be accessed by a given role, it should not be possible. There rights and roles should be very tight, to prevent abuse.

## Cases

[Airqualtiy](cases/airquality#Vulnerabilities)

## Bibliography

- <https://www.cpomagazine.com/tech/best-practices-for-authentication-and-authorization/>
