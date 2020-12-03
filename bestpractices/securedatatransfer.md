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

## Flaws
If an encryption is not implemented correctly or is missing, it leaves the opportunity to the hackers to sniff and listen to the unencrypted traffic. Hackers could gather important or personal data and use this data to advance furhter into the infrastructure. 

## Cases
The cases that are relevant to this best practice

## Bibliography
All sources used for thie specific subject. 

## Appendix
Any extra pages about this subject.