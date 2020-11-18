# Airquality sensor
Farms and workshops need clean air to operate their businesses.
So there can be a lot of stink or debris in the air, so there should be something to clean the air with.
An application, combinend with those sensors could fulfills this purpose: it takes the dirty air in, scrubs it, and clean air comes out.

## Table of Contents
- [Subject Explanation](#subject-explanation)
- [Strengths](#bibliography)
- [Vulnerabilities](#vulnerabilities)
- [Best practices](#best-practices)
- [Possible fixes](#possible-fixes)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Subject Explanation
According to the [cyber kill chain](https://www.varonis.com/blog/cyber-kill-chain/) the application and sensors were tested.
Testing was done on a server that was accessible to everyone.  <br /> The tools that were used are mostly the same tools we use in Kali Linux for other pentests. Among these are:
- Burp Suite
- Nmap
- Postman
- Security headers check

During the pentest the [research](%TODO) was kept in mind according to known IoT vulnerabilities. 

## Strengths
The application unfortunately didn't have a lot of strengths. Front - and back-end are both weak based on the
cyber security aspect.

## Vulnerabilities
The vulnerabilities in this case are as followed:

- **Broken authentication/authorization**  
If a user is logged in with a valid session, they can take that session and pretend they’re an admin. They can then create users, locations, and sensors. The endpoints aren’t protected, either. This means people can see what endpoints there are and what they return. 

- **Bad error handling**<br /> 
If there’s an error, the error messages will display too much information. Part of the code that regular users shouldn’t be able to see will be displayed. This is because the errors are handled badly. Hackers could take advantage of it.

- **No hashes for password** <br />
Passwords are not hashed and are stored as plain text in the database. This is a vulnerability that makes it easy for a hacker to see the passwords if they gained access to the database.

- **No Password rules**<br />
There aren’t any rules for the password when an account is created. This makes it possible to have a password with only one character or even no characters.

- **Input filtering** <br/> 
An attacker can make new users, sensors or locations and omit certain parameters and create invalid objects.

- **Outdated software** <br />
There are outdated maven dependencies, which can lead to possible vulnerabilities.

- **Weak JWT token**<br /> 
The JWT token is using a weak and guessable secret. This makes it possible to be brute-forced or guessed by the attacker

- **Insecure Headers** <br />
The security headers are not configured properly, which makes them vulnerable.

- **DOS attack**<br />
It is possible to attempt a Dos attack by sending a string to the Kafka server. This string will overload the server and cause services to stop.

- **Outside requests**<br />
The Kafka server is not protected against outside requests. This means anyone can send requests

- **Hardcoded Credentials**<br />
There are hardcoded credentials used in a .xml file. This means hackers could find and use these credentials for their own purposes.

## Best practices
The best practises, add refer! %TODO%

## Possible Fixes
All of the vulnerabilities in the application can be fixed. To fix those, for each vulnerability
the best practice needs to be followed. After this is done, there should be a lot of tests, to see if the vulnerabilities are
really fixed.

## Bibliography
- the document for the research of known vulnerabilities %TODO%

## Appendix 
Any extra pages about this subject.
