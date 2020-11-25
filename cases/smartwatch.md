# Smartwatch
Smartwatches are a common item in the average catalouge of items a persons carries around these days. It has your contact information, can make calls to your friends and even keep track of your steps.
But these watches are are not just like any ordinary watch, they can be hacked and used to spy on people.

## Table of Contents
- [Subject Explanation](#subject-explanation)
- [Strengths](#bibliography)
- [Vulnerabilities](#vulnerabilities)
- [Best practices](#best-practices)
- [Possible fixes](#possible-fixes)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Subject Explanation
The Smartwatch case is about the reseach we've done on the "Samgsung Gear S3 frontier" Smartwatch.<br />
The attack we tried was done by first: scanning all the avaible methods we can call withouth authorization of every interface from the watch.<br />
Then the attacker could write malware that would abuse the open methods from those interface to hijack Wifi/Bluetooth/Contact info etc.. (depending on the interface)

## Strengths
The Samsung Smart Watch was really strong in it strengths, there were no other open attack vectors for us to exploits except the outdated OS it was running.

## Vulnerabilities
**Outdated OS**
The OS was outdated with the version 4.0.0.4, this allowed unauthorized acces to methods from some interfaces on the watch. <br />

**Unauthorised Acces to Interfaces**
Some interfaces on the watch did not need authorised acces to be able to call their methods, therefore the attack could write malware that calls these methods to receive and change information like: contact info, screenshots of the current screen, change the bluetooth of wifi connection and more, depending on the interface.

## Best practices
The Smartwatch should be updated when given the chance to.<br />
Always set automatic update option on the phone smartwatch app to "ON".<br />
And if the user has one, link the Samsung account to the Smart Watch App on the phone.

## Possible Fixes
To prevent outdated software from being used the user needs to update their Samsung Watch application on their phone, and update their Samsung Smart Watch.<br />
This is relatifly easy to implement, by simply checking "the automatic update" feature.<br />

## Bibliography
https://nvd.nist.gov/vuln/detail/CVE-2018-16262 <br />
https://www.youtube.com/watch?v=3IdgBwbOT-g&feature=youtu.be

## Appendix 
Any extra pages about this subject.
