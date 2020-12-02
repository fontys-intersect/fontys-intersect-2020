# Certificates

An in-depth page about Certificates. In this page, it will be explained how it works and how it should be used.

## Table of Contents
- [Explanation](#explanation)
- [Uses](#uses)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Explanation 
A certificate is like a promise that the webserver is who they sey they are. With a certificate, you can be sure that your data is transferred over a secured connection. Trusted certificates are issued by Certificate Authorities, like IdenTrust, DigiCert, Sectigo, and more. A trusted certificate has a public key, and others can rely that the private keys will correspond to the public key. 

## Uses
**Secure Connection**
Certificates are used to secure the connection from a webserver to a browser. With this certificate, you can be assured that your connection is encrypted. There are also self-signed certificates; however, those aren't as secure. Self-signed certificates are signed by you instead of by a certificate authority. This means it's not trusted by the browser and may give a pop-up message, like "this website might not be secure."

**Trusted Certificates**
Trusted certificates are good against man in the middle attacks, for example. Since the connection is encrypted, it's not possible for someone to intercept your data. You can't impersonate a trusted certificate, either, since these certificates come from a trusted authority. 

## Flaws
**Authority Breach**
In rare events, a trusted certificate company may be breached, rendering all the trusted certificates issued by said company vulnerable for attacks. An example is from a Dutch certificate authority, DigiNotar. DigiNotar was breached in 2011, and hackers trusted certificates to other hackers. They were sending phishing emailsm pretending to be legit companies like Google. 

**Self-Signed Certificates**
Realistically, however, it's the self-signed certificate that you need to watch out for. If companies or other instances have a self-signed certificate, chances are that they tell people to ignore the warning their browsers give them. If the instance the website belongs to is breached, and a man-in-the-middle attack is attempted, it won't look different than it usually does and people may carelessly keep clicking until they are where they want to be. Any data they have will be in the hands of the hackers.

## Cases
The cases that are relevant to this best practice

## Bibliography
[DigiNotar](https://en.wikipedia.org/wiki/DigiNotar)
[Darknet Diaries, The Weakest Link](https://darknetdiaries.com/episode/3/)
[Security Certificate](https://www.thesslstore.com/blog/what-is-a-website-security-certificate-and-what-does-it-do-for-your-business/)

## Appendix
Any extra pages about this subject.