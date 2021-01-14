# Smartwatch

Smartwatches are a common item in the average catalogue of items a person carries around these days. It has your contact information, can make calls to your friends and even keep track of your steps. But these watches are not just like any ordinary watch, they can be hacked and used to spy on people.

## Table of Contents

- [Case Explanation](#case-explanation)
- [Strengths](#bibliography)
- [Vulnerabilities](#vulnerabilities)
- [Best practices](#best-practices)
- [Possible fixes](#possible-fixes)
- [Bibliography](#bibliography)

## Case Explanation

The smartwatch that was tested appeared to be running an outdated version of its firmware, allowing the testers to exploit known vulnerabilities

The attack we tried was done by first scanning all the available methods we can call without authorization of every interface from the watch. The program used here would call every method with random parameters and log the response get. If the response was "InvalidArgs" instead of "AccesDenied", that meant we could abuse the interface with the out of date OS version.

Then the attacker could write malware that would abuse the open methods from those interfaces to hijack Wifi/Bluetooth/Contact info etc.. (depending on the interface)

![smartwatch-diagram](/assets/images/smartwatch-diagram.PNG)

## Strengths

The SmartWatch was strong in its base security, meaning that the implementation the manufacturer implemented were working correctly.
We were unable to decipher the traffic from/to the watch and were not able to directly interact with the base functionalities like Wifi / Bluetooth.

there were no other open attack vectors for us to exploits except the outdated OS it was running.

## Vulnerabilities

**Outdated OS**
The OS was outdated, this allowed unauthorized access to methods from some interfaces on the watch because of a lack of security implementations regarding the D-Bus structure of the watch.

**Unauthorised Acces to Interfaces**
Some interfaces on the watch did not need authorized access to be able to call their methods, therefore the attack could write malware that calls these methods to receive and change information like: contact info, screenshots of the current screen, change the Bluetooth of wifi connection and more, depending on the interface.

## Possible Fixes

To prevent outdated software from being used the user needs to update their Watch application on their phone, and update their smartwatch.

This is relatively easy to implement, by simply checking "the automatic update" feature.

## Best practices

The Smartwatch should be updated when given the chance to as referred to in the [version update](/bestpractices/versionupdate) best practice.

Always set the automatic update option on the phone smartwatch app to "ON", making sure the user does not have to think about whether he has to update his watch or not. And if the user has one, link the account to the smartwatch app on the phone. This way the user can erase their data, or transfer their data to a new watch safely.

## Bibliography

- NIST. (z.d.). NVD - CVE-2018-16262. nvd.nist.gov. <https://nvd.nist.gov/vuln/detail/CVE-2018-16262>
