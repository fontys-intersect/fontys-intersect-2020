# Authorization

An in-depth page about the Best Practice at hand. In this page, it will be explained how it works and how it could be implemented.

## Table of Contents
- [Explanation](#explanation)
- [Uses](#uses)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Explanation 
**Validate Sessions**
When an entity calls a method, the application needs to know if this call is legit in its request. The entity has a session that it uses to validate its request. The backend needs to check if the session, tied to this specific user, has a right to exist or not. If not, terminate the user or deny the request.

**Validate user Role & permissions**
In the entity session, there's usualy information stored that the backend can use to identify the entity and the permissions it has. When the entity calls a method the user role is given as a parameter to the backend, it is then compared to the permissions certain users have to see if this current user has the permission to execute the command it requests.

## Uses
Authorization needs to be properly implemented. If the wrong entity has access to methods he has to business using, it could spell a lot of trouble.

The correct implementation should be to validate the session given by the entity when a call is made to make sure the entity has the right to be able to make a call, and the permissions of that entity need to be checked to make sure he has the right to call the specified method.

## Flaws
It is possible that, if a hacker has found a way around the the authorization process, this implementation would be useless. 

## Cases
[Airqualtiy](cases/airquality#Vulnerabilities)

## Bibliography
- [https://www.cpomagazine.com/tech/best-practices-for-authentication-and-authorization/](https://www.cpomagazine.com/tech/best-practices-for-authentication-and-authorization/)

## Appendix
Any extra pages about this subject.