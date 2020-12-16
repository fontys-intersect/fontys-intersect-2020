# Regular and Secure Version Updates

Systems are updated regularly, but these updates can pose a security risk if not done properly.

## Table of Contents

- [Explanation](#explanation)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Explanation

Every IoT device, from a light bulb to smart-watch, should be updated. When security issues are found, the devices should be able to be updated, so the found vulnerabilities can be fixed and closed. According to the Enisa: "If a dependency is vulnerable and exposed on the Internet, there may be severe consequences. Successful attacks based on outdated components are clear indicators that software dependencies should be taken seriously."(Enisa, 2019).

The update itself should be done securely so the system should check if it is performing a legitimate update to its firmware. The update must be transferred over a secure connection and verified before updating, this can be done with a simple hash.

## Flaws

When a device is supporting update functionality, it expands the attack surface. If the update is not verified and secured, the system can be taken over or damaged by a malicious software update.

## Cases

- [Smartscreen](cases/smartscreen#Vulnerabilities)

The smartscreen supported an update functionality, but in an insecure way. A malicious update could be sent to the updating client by intercepting the traffic.

- [Smartwatch](cases/smartwatch#Vulnerabilities)

The smartwatch was severely outdated, causing the possibility of unauthorised access to interfaces.

## Bibliography

- ENISA. (2017, November 20). Baseline Security Recommendations for IoT. <https://www.enisa.europa.eu/publications/baseline-security-recommendations-for-iot>
- Hogan, M., & Piccarreta, B. (2018, February). Draft NISTIR 82001 Interagency Report on Status of 2 International Cybersecurity 3 Standardization for the 4 Internet of Things (IoT). NIST. <https://csrc.nist.gov/CSRC/media/Publications/nistir/8200/draft/documents/nistir8200-draft.pdf>
- Enisa. (2019, 1 October). Good Practices IoT Enisa. ENISA. <https://www.enisa.europa.eu/publications/good-practices-for-security-of-iot-1/at_download/fullReport>
