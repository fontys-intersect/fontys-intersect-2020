# Airquality sensor

Farms and workshops need clean air to operate their businesses. There can be a lot of toxins or dust in the air, this should be monitored. The Airscrubber fulfills this purpose: it monitors the quality of the air. We are asked to test the security of the application.

## Table of Contents

- [Airquality sensor](#airquality-sensor)
  - [Table of Contents](#table-of-contents)
  - [Subject Explanation](#subject-explanation)
  - [Strengths](#strengths)
  - [Vulnerabilities](#vulnerabilities)
  - [Possible Fixes](#possible-fixes)
  - [Best practices](#best-practices)
  - [Bibliography (APA)](#bibliography-apa)

## Subject Explanation

The application and sensors were tested according the [cyber kill chain](https://www.varonis.com/blog/cyber-kill-chain/). Testing was done on a private server that was only accessible to the testers.

The tools that were used are mostly the same tools we use in Kali Linux for other pentests. Among these are:

- Burp Suite
- Nmap
- Postman
- [Security headers](https://www.securityheaders.com) check

During the pentest, the [research](/research) was kept in mind according to known IoT vulnerabilities.

## Strengths

The application unfortunately didn't have a lot of strengths. Front - and back-end are both weak based on the cybersecurity aspect.

## Vulnerabilities

The vulnerabilities, in this case, are as followed:

- **Broken authentication/authorization**
    If a user is logged in with a valid session, they can access all pages, because the server is not checking if they an administrator or not. They can then create users, locations, and sensors.

- **Bad error handling**
    If there’s an error, the error messages display very little to no information. This is very inconvenient to both the user and the developer because nobody can see what went wrong.

- **No hashes for password**
    Passwords are not hashed and are stored as plain text in the database. This is a vulnerability that makes it easy for a hacker to access and reuse the passwords if they gained access to the database.

- **No Password rules**
    There aren’t any rules for the password when an account is created. This makes it possible to have a password with only one character or even no characters.

- **Input filtering**
    An attacker can omit certain parameters when making new users, sensors or locations, making these invalid.

- **Outdated software**
    There are outdated maven dependencies, which can lead to possible vulnerabilities.

- **Weak JWT**
    The JWT is using a weak and guessable secret key. This makes it possible for the attacker to brute-force or guess it.

- **Insecure Headers**
    The security headers are not configured properly, which makes them vulnerable to attacks like clickjacking.

- **DOS attack**
    It is possible to make the system crash and unable to restart by sending a string to the Kafka server. This string will cause the server to crash and cause the backend service to stop and crash again on reboot.

- **Outside requests**
    The Kafka server is not protected against outside requests. This means anyone can send requests, resulting in the wrong or polluted data.

- **Hardcoded Credentials**
    There are hardcoded credentials used in a .xml file. Once an attacker has access to the system, they can use the credentials to pivot to other systems.

## Possible Fixes

All of the vulnerabilities in the application can be fixed. To fix those, for each vulnerability
the best practice needs to be followed. After this is done, there should be a lot of tests, to see if the vulnerabilities are
really fixed.

## Best practices

The best practices, add refer! %TODO%

## Bibliography (APA)

- the document for the research of known vulnerabilities %TODO -> add refer%
