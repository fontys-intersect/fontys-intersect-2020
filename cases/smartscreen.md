# Smartscreen

These days many companies and individuals use IoT devices, such as smartphones, smart doorbells or smart screens. The number of IoT devices grows significantly every year, most of these IoT devices are within businesses.

The smartscreen is a system which is popular in different types of companies, because of the flexibility of those screens. Smartscreens can run custom applications but can also be connected to a laptop to give presentations. Besides data attacks on the smartscreens, attackers could try to get control over the smartscreen to get network access or to use the smartscreen for malicious plans like a botnet. A botnet is a network of connected pc’s used for group attacks. Most of the time these pc’s are infected by malware and the owner is unaware of their participation in a botnet.

## Table of Contents

- [Case Explanation](#case-explanation)
- [Strengths](#strengths)
- [Vulnerabilities](#vulnerabilities)
- [Possible Fixes](#possible-fixes)
- [Best practices](#best-practices)

## Case Explanation

For the pentest, a test network was created and the screens were connected to the router with an ethernet cable. The pentesters had full network access and control. Physical access to the smartscreen was also granted to the pentesters. One of the screens has an android version as an operating system while the other had a custom operating system.

![network sketch](/assets/images/networksketch/smart-screen.png)

the screens and their services were tested according to the [cyber kill chain](https://www.varonis.com/blog/cyber-kill-chain/). This means the pentest started with reconnaissance, after enough data had been gathered the intrusion was started. When a successful intrusion is executed, it is time for the exploitation phase. After one or several successful exploits it is possible to try privilege escalation. If the privilege escalation is successful full system access is obtained.The pentests started the same way and became slightly different based on their findings. The tools that were used are mostly the same tools we use in Kali Linux for other pentests. Among these are:

- [Burp Suite](https://portswigger.net/burp)
- [Nmap](https://nmap.org/)
- [CallStranger](https://github.com/yunuscadirci/CallStranger)
- [Wireshark](https://www.wireshark.org/)

During the pentest, the [research](/research) into common IoT vulnerabilities was kept in mind.

## Strengths

The security of the tested smart screens was of a high level, most ports refused any connection and several vulnerabilities were already patched. Ports that aren't needed are closed and attack vectors have been minimalized.

## Vulnerabilities

- **Android Debug Bridge**
The initial version of the smart screen we tested had the android debug bridge(ADB) port opened, this means anyone on the network can get a root shell on the smart screen. The company explained that the first firmware version was a development version due to internal confusion.

![ADB connect](/assets/images/adb_connect.png)

After contacting the company about the ADB port they ask the pentesters to do a firmware update with the latest production version. Eager to find out if the port was actually closed the pentesters  did another network scan. This scan proves the port is closed on the production version.

- **False firmware update**
Because the update server did not implement HTTPS it is possible to read the communication between the smart screen and the server. The pentesters used a proxy to capture individual requests and responses. By altering certain requests it is possible to find all responses from the server. This makes it possible to create a fake update server, combine this with a man in the middle attack and it is possible to make the smart screen pull an update from the fake server. This can allow an attack to add malware or corrupt the smart screen.

![update requests](/assets/images/fake_server.png)

## Possible Fixes

Both problems can be fixed quite easily. For the ADB vulnerability just make sure no production version has the ADB port open and make sure no one gets the developer version.The company should build in a check before delivering screens to any one, this includes screens normally used for internal testing. To secure the server an SSL certificate should be added to the server and this certificated should be checked if it's trusted. The company should build in a check before delivering screens to any one, this includes screens normally used for internal testing. A self-signed certificate can be forged by an attacker which makes it useless in this case. A trusted SSL certificate cost money but this is way less than the potential cost of a security breach.

## Best practices

The best practice connected to the ADB port is [split development and production](/bestpractices/splitdevprod). This best practice describes why it is important to have this separation and how to do it.

The best practices connected to the firmware update are [certificates](/bestpractices/certificates) and [secure data transfer](/bestpractices/securedatatransfer). Both these best practices describe the importance of encryption, they both focus on a different part but they are both connected to this case. The Certificate best practice is the most important one for this vulnerability.

The last best practice that is applicable to this case is [versionupdate](/bestpractices/versionupdate) update. There were a few outdated libraries that were used, but all vulnerabilities for this library seem to be patched. However it stays important to update all libraries used to profit from their security fixes.

more about these best practices can be read on their respective pages.
