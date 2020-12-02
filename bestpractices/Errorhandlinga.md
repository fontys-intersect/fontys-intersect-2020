# Error Handling

This page will go in-depth on the topic of error handling; what it is, why it's important, and how it could be implemented securely.

## Table of Contents
- [Explanation](#explanation)
- [Uses](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)
- [Appendix](#appendix)

## Explanation 
Error handling is important for running a smooth application. If anything happens, the error will be caught and handled internally, while showing a basic message to the user what might have gone wrong without giving out too much information. If there are any unhandled errors, and the website crashes, the website will stop working or not work as intended. The information that's shown in the error will give hackers a basic idea what language it's written in, what technologies are used, and much more. 

## Usage
Error handling is used in any code, from applications to backends and other software. Good error handling goes hand in hand with good testing. 

## Flaws
There may still be errors around that the developers might not have noticed. These errors might still give some useful information to the hackers. And if the errors are correctly handled, but the error messages are too informational, the hacker might still reason what might be happening behind the scenes. 

## Cases
The cases that are relevant to this best practice

## Bibliography
[Owasp Error Handling](https://owasp.org/www-community/Improper_Error_Handling)

## Appendix
Any extra pages about this subject.