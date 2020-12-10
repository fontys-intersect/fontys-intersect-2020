# Monitoring and Logging

An in-depth page about Monitoring and Logging. In this page, it will be explained how it works and how it could be implemented.

## Table of Contents

- [Explanation](#explanation)
- [Uses](#uses)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

A lot of things happen within your application or website. Knowing what is going on and where is very important. Monitoring your application and logging what happens will help to alert when something is wrong. You can use several different applications or frameworks to monitor or log, but the output is the same; it'll tell you if there are too many login attempts, for example. You can use different tactics to stop this. Loggin is not only important for security, but also for debugging and the general ease of use for the developers and testers.

The difference between monitoring and logging is that monitoring actively prevents things from happening, such as users sending malicious requests. Whereas logging just saves the information of the events, for tracing back the steps.

## Uses

When you monitor your application, you will know what is happening and how users are using your application. If you can see someone attempting to hack into your website, the monitoring system will issue a warning and try and stop it. Thanks to logging you will also know what damage will have been done and how you can prevent attacks in the future.

## Flaws

It's important to finetune the monitoring system; overreporting can be just as dangerous as underreporting. If you see every single click someone is making, you won't be able to tell when something is coming from a hacker through the slew of warnings and mentions you'll be getting. This can be called false positives, the application thinks something is wrong when there is no problem. The other issue is false negatives, where the application thinks that everything is right, while damage is being done. It is important to fine-tune your logging, luckily there are a lot of frameworks and guidelines on implementing logging and monitoring.

## Cases

- [Smartscreen](cases/smartscreen#Vulnerabilities)
  Not Applicable

- [Airquality](cases/airquality#Vulnerabilities)
	Not Applicable

- [Smartscreen](cases/smartscreen#Vulnerabilities)
	Not Applicable

## Bibliography

- [Owasp](https://owasp.org/www-project-top-ten/2017/A10_2017-Insufficient_Logging%2526Monitoring)
%TODO% more sources as mentioned in the text (frameworks and guidelines)
