# Authorization

Authorization is always called in the same breath as Authentication, and sometimes even used interchangably, even though they are two very separate things. Authentication is making sure you are who you are, and authorization is telling people what they can or can't do once they're in the system. In this page, we're going to talk about Authorization.

## Table of Contents

- [Explanation](#explanation)
- [Usage](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

**Validate Sessions**
 
When an entity calls a method, the application needs to know if this call is legit in its request. The entity has a session that it uses to validate its request. The backend needs to check if the session, tied to this specific user, has a right to exist or not. If not, terminate the user or deny the request.

**Validate user Role & permissions**
Information on the user and its role is stored in the session. Since this is stored client-side, it is important to make sure that the user cannot change it, this can be done by using a JWT-token. When the entity calls a method the user role is given as a parameter to the backend, it is then compared to the permissions certain users have to see if this current user has the permission to execute the request.

## Uses
Authorization needs to be properly implemented. If the wrong entity has access to methods he has to business using, it could spell a lot of trouble. The correct implementation should be to validate the session given by the entity when a call is made to make sure the entity has the right to be able to make a call, and the permissions of that entity need to be checked to make sure he has the right to call the specified method.

If you want to know more about authentication in IoT, [Cloud Security Alliance](https://downloads.cloudsecurityalliance.org/assets/research/internet-of-things/identity-and-access-management-for-the-iot.pdf) has created a more in-depth guideline to oversee identity and access management.

## Flaws

A flaw that was found in the air quality project was that the session was not checked on roles, only whether it exists or not. This meant that any user that is logged in could access every page, regardless of his role. It is important that all sessions and their roles are validated.

To make sure that the users cannot do too much, it also is important that any given user does not have too many rights. If it does not needs to be accessed by a given role, it should not be possible. There rights and roles should be very tight, to prevent abuse.

## Cases

- [Airquality](cases/airquality#Vulnerabilities)

There was no checking on who made the requests to the server, so every user can acces all pages.

- [Smartwatch](cases/smartwatch#Vulnerabilities)

The smartwatches had bad authorization, the user could acces and abuse certain interfaces.

## Bibliography

- <https://www.cpomagazine.com/tech/best-practices-for-authentication-and-authorization/>
