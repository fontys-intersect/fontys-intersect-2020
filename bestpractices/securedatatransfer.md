# Secure Data Transfer and Storage

An in-depth page about Secure Data Transfer and data storage. In this page, it will be explained how it works and how it could be implemented. 

## Table of Contents

- [Secure Data Transfer and Storage](#secure-data-transfer-and-storage)
- [Table of Contents](#table-of-contents)
- [Explanation](#explanation)
- [Usage](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

Internet traffic can be red or even changed by anyone on the same network, there is very little to solve this on a small scale network. To make sure that the sniffed data is not usable, encryption should be used. Encryption comes in many forms, but most traffic (i.e. `HTTP`, `FTP`, `SMTP`, etc.) supports `SSL/TLS`. SSL is a powerful widely used encryption. Its most common use is for web traffic, however, multiple protocols support it. If for any reason the protocol is unable to use SSL, there are many variants of encryption, such as end-to-end, peer-to-peer and VPN.

## Usage

In encryption it is important to be consistent. This means that every form of communication is encrypted to ensure that no information leaks.

## Flaws

If encryption is not implemented correctly or is missing, it leaves the opportunity to the hackers to sniff and listen to the unencrypted traffic. Hackers could gather important or personal data and use this data to advance further into the infrastructure.

Proper encryption is extremely difficult to break, so it has no real flaws. However, there is a lot to do wrong in encryption. First of all, use the latest version of an up to date encryption standard. In software it is always very important to use an up to date framework, no matter how good you are, developing your own encryption is never very secure. Look into the different variants of encryption and make sure that the correct version is used. The wrong version can lead to problems and insecurity. In almost all situations it is best practice to use asymmetric encryption, this means that the key to encrypt is different from the key to decrypt. This way you can make sure that the people that can encrypt data can not decrypt it. This means attackers also cannot decrypt them. Only the intended receiver can read the send data.

## Cases

- [Airquality](cases/airquality#Vulnerabilities)

There was a distinct lack of encryption of any encryption on the air quality project, leaving the system vulnerable.

- [Smartscreen](cases/smartscreen#Vulnerabilities)

The smart screen also lacked encryption where needed, the update system. This allowed us to spoof a malicious update.

- [Smartwatch](cases/smartwatch#Vulnerabilities)

The smartwatches had the secure transfer done really well. We were unable to find problems with the encryption.

## Bibliography

- Allan, M. (2020, June 22). 6 types of encryption that you must know about. GoodCore Blog. [https://www.goodcore.co.uk/blog/types-of-encryption/]
