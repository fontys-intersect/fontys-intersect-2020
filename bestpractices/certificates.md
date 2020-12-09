# Certificates

An in-depth page about Certificates. In this page, it will be explained how it works and how it should be used.

## Table of Contents

- [Explanation](#explanation)
- [Uses](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

A certificate is like a promise that the webserver is who they say they are. With a certificate, you can be sure that your data is transferred over a secured connection. Trusted certificates are issued by Certificate Authorities, like IdenTrust, DigiCert, Sectigo, and more. The certificate proves that the SSL connection is safe and has not been tampered with by a hacker.

## Usage

**Secure Connection**
Certificates are used to secure the connection from a web server to a browser. With this certificate, you can be assured that your connection is encrypted. There are also self-signed certificates; however, those aren't as secure. Self-signed certificates are signed by you instead of by a certificate authority. This means it's not trusted by the browser and may give a pop-up message, like "this website might not be secure."

**Trusted Certificates**
Trusted certificates are the solution against man in the middle attacks. Since the connection is encrypted, it is not possible to intercept the data. You can't impersonate a trusted certificate, either, since these certificates come from a trusted authority. This means that the data cannot be tampered with, since that would make the certificate invalid, making sure that all the data send is valid.

**Enisa Guideline**
Enisa has made an in-depth document where it explains the imporance of web certificates and how they should be used. You can read it [here.](assets/pdf/EnisaWebCertificateGuidelines.pdf)

## Flaws

**Authority Breach**
In rare events, a trusted certificate company may be breached, rendering all the trusted certificates issued by said company vulnerable for attacks. An example is from a Dutch certificate authority, DigiNotar. DigiNotar was breached in 2011, and hackers trusted certificates to other hackers. They were sending phishing emails pretending to be legit companies like Google. If this happens, all certificates issued by this party needs to be renewed, the issuer should publish the details on the leak, so people can fix the issues.

**Self-Signed Certificates**
Realistically, however, it's the self-signed certificate that you need to watch out for. If companies or other instances have a self-signed certificate, chances are that they tell people to ignore the warning their browsers give them. If the instance the website belongs to is breached, and a man-in-the-middle attack is attempted, it won't look different than it usually does and people may carelessly keep clicking until they are where they want to be. Any data they have will be in the hands of the hackers.

**Bad certificate management**
Another big problem is badly managed certificates. certificates that have expired, are self-signed or are not properly configured. This damages the integrity of the encryption and makes it very easy the exploit the connection.

## Cases

%TODO%

## Bibliography

- [DigiNotar](https://en.wikipedia.org/wiki/DigiNotar)
- [Darknet Diaries, The Weakest Link](https://darknetdiaries.com/episode/3/)
- [Security Certificate](https://www.thesslstore.com/blog/what-is-a-website-security-certificate-and-what-does-it-do-for-your-business/)