# Research

## Theory

Before we started this project we looked into the existing guidelines written by other people and organizations. This gave us a pretty clear insight into the requirements of a good general guideline. These three are the best guidelines we could find:

- [OWASP IoT Top 10](https://owasp.org/www-pdf-archive/OWASP-IoT-Top-10-2018-final.pdf)
  The OWASP IoT top ten is a quick overview of the ten most common IoT vulnerabilities. It does not go into much detail but it is a great start for more detailed guidelines.
- [enisa good practices for security of iot](https://www.enisa.europa.eu/publications/good-practices-for-security-of-iot-1)
  This Enisa guide focuses mainly on the software development lifecycle it gives great ways for developers of IoT to improve their development lifecycle.
- [Guidelines for Overcoming some IoT Security Issues](https://www.iim.ftn.uns.ac.rs/is17/papers/33.pdf)
  This guideline gives common attacks and what users can do to minimize the attack vectors.

These three formed the base for our research into IoT devices and their guidelines. These guidelines are a great start but all lack on certain points.

The OWASP top 10 is a quick list of common vulnerabilities. It lacks proper explanations for the named vulnerabilities and does not suggest any solutions. This list is great to do a quick check for developers but requires further research per topic if one of the issues has not been handled yet.

The Enisa guide is really good for setting up a secure development lifecycle but it does not talk about common vulnerabilities. There are a few examples but those are limited. Furthermore, this guideline is focused on developers only.

the guideline for overcoming some IoT security issues is a proper read for IoT users who have a lot of technical knowledge in device and network management. It however lacks the explanation for inexperienced users.

### other contesters

besides the three best guidelines we also look into these other guidelines.

- [nistir 8259A](https://nvlpubs.nist.gov/nistpubs/ir/2020/NIST.IR.8259A.pdf)
  this guideline describes the options a developer should add to IoT device management options because it describes such a small part it did not make the top 3.
- [nistir 8228](https://nvlpubs.nist.gov/nistpubs/ir/2019/NIST.IR.8228.pdf)
  This guideline focuses on IoT management and does not go beyond this subject, meaning it's not the most ideal basis for the intersect guidelines.
- [enisa securing smart infrastructure in covid 19 pandeminc](https://www.enisa.europa.eu/news/enisa-news/securing-smart-infrastructure-in-covid-19-pandemic)
  this guideline gives a few tips for home and business users but it lacks explanations of these tips. This is a very short document that is not extensive enough to form a proper base.
- [enisa baseline security recommendations for IoT](https://www.enisa.europa.eu/publications/baseline-security-recommendations-for-iot)
  this one came close to being in the top 3. The reason it did not make it is because of the lack of depth. it gives a lot of useful baselines but it does not explain enough.
- [GSMA IoT security guidelines](https://www.gsma.com/iot/wp-content/uploads/2020/05/CLP.11-v2.2-GSMA-IoT-Security-Guidelines-Overview-Document.pdf)
  The GSMA guidelines where another close contender. It clearly states the different challenges and an approach to fix these challenges. but it does not give concrete solutions and it focuses too much on the mobile network.
- [trend micro smart yet flawed: IoT device vulnerabilities explained](https://www.trendmicro.com/vinfo/us/security/news/internet-of-things/smart-yet-flawed-iot-device-vulnerabilities-explained)
  This is more a news article than actual guidelines and it only mentions three common vulnerabilities. because it is not a scientific article it did not make the top three.
- [A Comprehensive Study of Security and Privacy Guidelines, Threats, and Countermeasures: An IoT Perspective](https://www.mdpi.com/2224-2708/8/2/22)
  this document focuses on two levels of a cisco proposed structure. These levels are the node and communication levels. It properly explains these levels but completely ignores other levels like the data levels and user level. Because it has a limited focus it did not make our top three.

  a useful tool we used is [the Enisa IOT tool](https://www.enisa.europa.eu/topics/iot-and-smart-infrastructures/iot/good-practices-for-iot-and-smart-infrastructures-tool). This tool splits the IoT world into different sections, like smart hospitals and industry 4.0. for each section, it gives sources that apply to that industry sector.

## Pentest

Our main research was based on pentests of real IoT devices. For the sake of privacy and security, we cannot publish the tested devices, but we can explain their type. These devices were tested:

- Smartboard
        - This is a smartboard running android, mainly used in schools and board rooms. This product is also used in practice. The smartboard can both run its programs and be connected to a laptop or pc.

- Industrial air quality control system
        - This project has a backend server, a web interface, and several connected sensors. These sensors measure several air properties, the backend processes this date and the frontend shows graphs of the measurements. this way the clients can keep an eye on the air quality.

- Smartwatch(es)
        - This device has a frontend, backend and some built-in sensors. Smartwatches are mostly used to monitor health, save time and money.
