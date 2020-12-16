# Secret Management

During the development and usage of systems, secrets are used to communicate with other systems. These secrets must remain secrets, or they could be abused by attackers

## Table of Contents

- [Secret Management](#secret-management)
  - [Table of Contents](#table-of-contents)
  - [Explanation](#explanation)
  - [Usage](#usage)
  - [Flaws](#flaws)
  - [Cases](#cases)
  - [Bibliography](#bibliography)

## Explanation

All the secrets including the private keys used for encryption should be stored in a secured place. If those secrets and keys are exposed to the public and aren't properly hidden, it will be an easy task for the hackers to break the encryption and the security mechanisms.

## Usage

Secrets such as private keys, credentials and configuration files should not be leaked, since they can be abused very easily. That is why all these secrets need to be stored in one central system, such as a vault or a secret manager, they need to be stored [encrypted](https://www.ekransystem.com/en/blog/secrets-management) at the very minimum. This makes sure that only the system with permission can access the secrets. It can even be argued that not all developers need access to the secrets, to minimize the chance of the secrets leaking.

## Flaws

Even if the secrets are stored in a safe place, they must be still accessible. The connection and data transfer between the storage and the program should also be encrypted, or the secret will still be obtainable by a hacker.

## Cases

- [Airquality](cases/airquality#Vulnerabilities)

There is one case reported from the penetration tests related to this security issue: There where hardcoded credentials in an XML file in the airquality project.

## Bibliography
[Ekransystem: Secret management blogpost, November 26 2019](https://www.ekransystem.com/en/blog/secrets-management)
[Secret Management, Date: n.d.](https://www.cyberark.com/what-is/secrets-management/)
