# Secure Data Transfer and Storage

An in-depth page about Secure Data Transfer and data storage. In this page, it will be explained how it works and how it could be implemented. 

## Table of Contents
- [Secure Data Transfer and Storage](#secure-data-transfer-and-storage)
  - [Table of Contents](#table-of-contents)
  - [Explanation](#explanation)
  - [Uses](#uses)
  - [Flaws](#flaws)
  - [Cases](#cases)
  - [Bibliography](#bibliography)
  - [Appendix](#appendix)

## Explanation 
Whatever you do, data will go from point A to point B, and data at point B will have to be stored, to be retrieved again later. It is very important that this happens as securely and safely as possible.

## Uses
All the communication between the IoT devices and the Internet should be encrypted. The SSL/TLS encryption should be used where appropriate. This requires the use of cryptographic algorithms. Storage should also be encrypted and stored in a database. That database should be in a safe place in the infrastructure, preferrably non-internet-facing. 

## Explanation

Internet traffic can be red or even changed by anyone on the same network, there is very little to solve this on a small scale network. In order to make sure that the sniffed data is not usable, encryption should be used. Encryption comes in many forms, but most traffic (i.e. `http`, `ftp`, `smtp`, etc.) supports `SSL/TLS`. SSL is a powerful a widely used encryption. Its most common use is for webtraffic, however, multiple protocols support it. If for any reason the protocol is unable to use SSL, there are many variants of encryption, such as end-to-end, peer-to-peer and VPN.

## Usage

In encryption it is important to be consistent. This means that every form of communication is encrypted to ensure that no information leaks.

## Flaws
If an encryption is not implemented correctly or is missing, it leaves the opportunity to the hackers to sniff and listen to the unencrypted traffic. Hackers could gather important or personal data and use this data to advance furhter into the infrastructure. 

Proper encryption is extremely difficult to break, so it has no real flaws, however, there is a lot to do wrong in encryption. First of all, use the latest version of an up to date encryption standard. In software it is always very important to use an up to date framework, no matter how good you are, developing your own encryption is never very secure. Look into the different variants of encryption and make sure that the correct version is used. The wrong version can lead to problems and insecurity. In almost all situations it is best practice to use asymmetric encryption, this means that the key to encrypt is different from the key to decrypt. This way you can make sure that the people that can encrypt do not  

## Cases

The cases that are relevant to this best practice

## Bibliography

All sources used for the specific subject.

## Appendix

Any extra pages about this subject.
