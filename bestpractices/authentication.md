# Authentication
This page will go in-depth on the topic of authentication; what it is, why it's important, and how it could be implemented securely.

## Table of Contents
- [Explanation](#explanation)
- [Usages](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Explanation 
If you have an application, you don't want to have people snooping around behind the scene. That's where authentication comes in; this process verifies that someone or something is who it claims to be. Certain users, entities or websites will have permission and power to do what others can't, such as reading or writing into the system or accessing certain pages.

## Usage
- **User ID's**
To start with, users should have User ID's. These User ID's should be case-insensitive. This is to avoid confusion. ID's should also be unique. You can have your E-mail address as your ID, but you should make sure to apply input validation, to make sure that the e-mail is structured like a valid e-mail. If you have a normal application, it's okay to keep the User ID public, but if you have an application that requires secrecy, it'd be better to have them assigned and kept secret. 

- **Passwords**
This is the most important part. Passwords should meet several requirements to be secure. They should have a minimum length of 8 characters, or they're too weak. They should be allowed to have any characters in them, to make it harder to crack. You should also set an upper limit of characters, to make sure there aren't any Long Password Denial of Service attacks. Store passwords securely, encrypted in a database. Make sure passwords aren't sent over insecure channels. Rotate passwords over set times; if a password is leaked, reset it before too much harm can be done. 

- **Two Factor Authentication**
Sometimes, just a password isn't enough. 2FA is a good way to authenticate your user. An extra, one-time code will be used to make sure you are really who you say you are. This is also a good way to prevent automated attacks, such as brute forcing. 

- **NIST Digital Identity**
Another source for authentication is the NIST document. NIST stands for the National Institute of Standards in Technology, based in America. In this guideline, authentication is explained even more in-depth. In bibliography will be a link to their authentication page.

## Flaws
The biggest flaw left is human error. Shoulder surfing is a pretty common way to find a password. If someone writes down a password, it doesn't matter how secure it is - people could steal it. Make sure a password is easy enough to remember, but not too guessable, while still being complex enough. Finding that balance can be hard. 

## Cases
%TODO%

## Bibliography
- [NIST Digital Identity](https://pages.nist.gov/800-63-3/sp800-63b.html)
- [OWASP cheat sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)


## Appendix
Any extra pages about this subject.