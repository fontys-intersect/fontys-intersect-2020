# Smartwatch
The Smartwatch Case, with information regarding the pentest done on the Samsung Gear S3 Frontier Smartwatch. (other name: Galaxy Smartwatch)

## Table of Contents
- [Subject Explanation](#subject-explanation)
- [Strengths](#bibliography)
- [Vulnerabilities](#vulnerabilities)
- [Best practices](#best-practices)
- [Possible fixes](#possible-fixes)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Subject Explanation
An in-depth explanation about the subject of the page. An explanation on how the attack can be executed and what the risks are.
The Smartwatch case is about the reseach we've done on the "Samgsung Gear S3 frontier" Smartwatch.
The attack we tried was done by first: scanning all the avaible methods we can call withouth authorization of every interface from the watch.
Then the attacker could write malware that would abuse the open methods from those interface to hijack Wifi/Bluetooth/Contact info etc.. (depending on the interface)

## Strengths
Secure in every way except the out of date OS (Tizen).

## Vulnerabilities
The OS was outdated with the version 4.0.0.4.

## Best practices
Update when connecting to phone.
Set automatic update option on phone.
If possible, link Samsung account.

## Possible Fixes
Several possible solutions, their effectiveness, their implementation difficulties and maybe an example.
To prevent outdated software from being used the user needs to update their Samsung Watch application on their phone, and update their Samsung Smart Watch.
This is relatifly easy to implement, by simply checking "the automatic update" feature.

## Bibliography
https://nvd.nist.gov/vuln/detail/CVE-2018-16262
https://www.youtube.com/watch?v=3IdgBwbOT-g&feature=youtu.be

## Appendix 
Any extra pages about this subject.
