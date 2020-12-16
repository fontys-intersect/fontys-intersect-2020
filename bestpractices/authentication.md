# Authentication

Authentication is always called in the same breath as Authorization, and sometimes even used interchangeably, even though they are two very separate things. Authentication is making sure you are who you are, and Authorization is telling people what they can or can't do once they're in the system. In this page, we're going to talk about Authorization.

## Table of Contents

- [Explanation](#explanation)
- [Usages](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

If you have an application, you don't want to have people snooping around behind the scene. That's where authentication comes in; this process verifies that someone or something is who they claim to be. Certain users, entities, or websites will have permission and power to do what others can't, such as reading or writing into the system.

## Usage

- **User ID's**
To start with, users should have User IDs. IDs should always be unique. You can have your E-mail address as your ID, but you should make sure to apply input validation. A number or GUID can also be a great user-ID, this makes it hard to guess and can be kept private very easy since the user has no reason for knowing it. It is better to keep the ID's secret since they could be abused.

- **Passwords**
This is the most important part. Passwords should meet several requirements to be secure. They should have a minimum length of 8 characters, or they're too weak. They should be allowed to have any characters in them, to make it harder to crack. You should also set an upper limit of characters, to make sure there aren't any Long Password Denial of Service attacks. This limit should be very high, as far as 100 characters; you don't want to limit the user when making a secure password, so forcing them to make a password of less than 20 characters is a bad idea.

Store passwords securely, hashed in a database. Hashing is similar to encryption, but only one-way. This means that you can create a hash of a password to compare it to the stored hash, but you cannot get the password from the hash. Also, make sure that all communication of credentials goes over a secured line, see [Secure data transfer](securedatatransfer) for more information.

- **Two Factor Authentication**
2FA is a good way to authenticate your user. 2FA is an extra one time code, that is sent to another confirmed device, such as a phone. This makes the login considerably more secure since the login must be confirmed by the user, even if the credentials are leaked.

- **NIST Digital Identity**
Another source for authentication is the NIST document. NIST stands for the National Institute of Standards in Technology, based in America. In this guideline, authentication is explained even more in-depth. (NIST Digital Identity, 2020).

**Validate Sessions**
Besides the passwords, the application also needs to know if the user is logged in. This can be done by using a session, for instance with JWT. This way the application knows who the user is and whether he is allowed something. Make sure that this session is secure since users can often edit the sessions client-side. JWT uses a signed hash to verify the integrity of the token, this makes sure that the token has not been tampered with.

## Flaws

The biggest flaw left is human error. Shoulder surfing is a pretty common way to find a password. If someone writes down a password, it doesn't matter how secure it is - people could steal it. Make sure a password is easy enough to remember, but not too guessable, while still being complex enough. Finding that balance can be hard.

If passwords ever do get leaked, don't hide it. This is illegal by GDPR and also a bad idea. Telling your users that something happened is very important so that they change their passwords after leaking.

Lastly, don't underestimate the importance of authentication. If you forget it, most other security solutions can be nullified. Make sure that everything is closed down and that only the correct users can access certain resources.

## Cases

- [Smartwatch](cases/smartwatch#Vulnerabilities)

The smartwatches had bad authentication, the user could access and abuse certain interfaces.

## Bibliography

- NIST Special Publication 800-63B. (z.d.). NIST. <https://pages.nist.gov/800-63-3/sp800-63b.html>

- Authentication - OWASP Cheat Sheet Series. (z.d.). cheatsheetseries.owasp.org. <https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html>
