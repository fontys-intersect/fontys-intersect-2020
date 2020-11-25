# Authentication
This page will go in-depth on the topic of authentication; what it is, why it's important, and how it could be implemented.

## Table of Contents
- [Explanation](#explanation)
- [Uses](#uses)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)
- [Appendix](#appendix)
## Explanation 
If you have an application, you don't want to have people snooping around behind the scene. That's where authentication come in; this process verifies that someone or something is whom it claims to be. Certain users, entities or websites will have permission and power to do what others can't, such as reading or writing into the system. 

## Uses
- **User ID's**
To start with, users should have User ID's. These User ID's should be case-insensitive. This is to avoid confusion. ID's should also be unique. You can have your E-mail address as your ID, but you should make sure to apply input validation. If you have a normal application, it's okay to keep the User ID public, but if you have an application that requires secrecy, it'd be better to have them assigned and kept secret. 

- **Passwords**
This is the most important part. Passwords should meet several requirements to be secure. They should have a minimum length of 8 characters, or they're too weak. They should be allowed to have any characters in them, to make it harder to crack. You should also set an upper limit of characters, to make sure there aren't any Long Password Denial of Service attacks.

Store passwords securely, encrypted in a database. Make sure passwords aren't sent over insecure channels. Rotate passwords over set times; if 

## Flaws
The biggest flaw left is human error. If someone writes down a password, it doesn't matter how secure it is

## Cases
The cases that are relevant to this best practice

## Bibliography
All sources used for thie specific subject. 

## Appendix
Any extra pages about this subject.