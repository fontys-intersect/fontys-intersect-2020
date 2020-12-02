# Smartscreen

Nowadays many companies or just people use IoT technologies; such as smartphone, smart bell or smart screen.
The smartscreen is a system which is popular in many (big) companies. Those screens store a lot of (sensitive) data, but for sure
those screens needs to be secure.

## Table of Contents

- [Subject Explanation](#subject-explanation)
- [Strengths](#strengths)
- [Vulnerabilities](#vulnerabilities)
- [Possible Fixes](#possible-fixes)
- [Best practices](#best-practices)
- [Bibliography (APA)](#bibliography-apa)
- [Appendix](#appendix)

## Subject Explanation

According to the [cyber kill chain](https://www.varonis.com/blog/cyber-kill-chain/) the screen and accorded services were tested. The tools that were used are mostly the same tools we use in Kali Linux for other pentests. Among these are:

- Burp Suite
- Nmap
- CallStranger
- wireshark

During the pentest the [research](/research) was kept in mind according to known IoT vulnerabilities.

## Strengths

The security of the tested smart screens was of a high level, most ports refused any connection and server vulnerabilities where already patched. Ports that aren't needed are closed and attack vectors have been minimalised.
The good aspects in the case/application

## Vulnerabilities

- **Android Debug Bridge**
The initial version of the smart screen we tested had the android debug bridge(ADB) port opened, this means anyone on the network can get a root shell on the smart screen.

- **False firmware update**
Because the update server did not implement https it is possible to read the communication between the smart screen and the server. This makes it possible to create a fake update server, combine this with a man in the middle attack and it is possible to make the smart screen pull an update from the fake server. This can either corrupt or add malware to the smart screen.

## Possible Fixes

Both problems can be fixed quite easily. For the ADB vulnerability just make sure no production version has the adb port open and make sure no one gets the developer version. To secure the server a ssl certificate should be added to the server.

## Best practices

The best practises, add refer! %TODO%

## Bibliography (APA)

- the** document for the research of known vulnerabilities %TODO%

## Appendix

Any extra pages about this subject.
