# Secret Management

An in-depth page about Secret management. In this page, it will be explained how it works and how it could be fixed. 

## Table of Contents

- [Secret Management](#secret-management)
- [Table of Contents](#table-of-contents)
- [Explanation](#explanation)
- [Usage](#Usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

All the secrets including the private keys used for encryption should be stored in a secured place. If those secrets and keys are exposed to the public and aren't properly hidden, it will be an easy task for the hackers to break the encryption and the security mechanisms.

## Usage

Secrets such as private keys, credentials and configuration files should not be leaked, since they can be abused very easily. That is why all these secrets need to be stored in one central system, such as a vault or a secret manager, they need to be stored encrypted as the very minimun. This makes sure that only the system with permission can access the secrets. It can even be argued that not all developers need access to the secrets, to minimize the chance of the secrets leaking.

## Flaws

Even if the secrets are stored in a safe place, it is important that they are still accessible. It should be made sure that the connection and data transfer between the storage and the program is also encrypted, or the secret will still come out.

## Cases

%TODO%

## Bibliography

[Secret Management](https://www.cyberark.com/what-is/secrets-management/)