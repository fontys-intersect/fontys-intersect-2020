# Regular and Secure Version Updates
An in-depth page about the Best Practice at hand. In this page, it will be explained how it works and how it could be fixed. 

## Table of Contents
- [Regular and Secure Version Updates](#regular-and-secure-version-updates)
  - [Table of Contents](#table-of-contents)
  - [Explanation](#explanation)
  - [Flaws](#flaws)
  - [Cases](#cases)
  - [Bibliography](#bibliography)
  - [Appendix](#appendix)

## Explanation 
Every IoT device, from a light bulb to smart watch, should be able to be updated. When security issues are found, the devices should be able to be updated, so the found vulnerabilities can be fixed and closed. 

The update itself should be done securely so the system should check if it is performing legitimate update to its firmware. This is done by using signing. The software should be signed with certificate and the device should check if the certificate has the right signature on it, in order to allow each update.

## Flaws
When a device is supporting update functionality, it expands the attack surface. If the update is not verified and secured by certificate, this can lead to security flaws and corrupting the system.

## Cases
The cases that are relevant to this best practice

## Bibliography
[Baseline Security Recommendations for IoT](https://www.enisa.europa.eu/publications/baseline-security-recommendations-for-iot)

[International Cybersecurity Standardization for IoT](https://csrc.nist.gov/CSRC/media/Publications/nistir/8200/draft/documents/nistir8200-draft.pdf)

## Appendix
Any extra pages about this subject.
