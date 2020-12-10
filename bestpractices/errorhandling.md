# Error Handling

This page will go in-depth on the topic of error handling; what it is, why it's important, and how it could be implemented securely.

## Table of Contents

- [Explanation](#explanation)
- [Uses](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

Error handling is important for running a smooth application. If anything happens, the error will be caught and handled internally, while showing a basic message to the user what might have gone wrong without giving out too much information. If there are any unhandled errors, and the website crashes, the website will stop working or not work as intended. A good rule of thumb is that if it is a clientside error show as much information as possible and if it is a serverside error, leak as little information as possible.

## Usage

Error handling is used in any code, from applications to backends and other software. Good error handling goes hand in hand with good testing.

## Flaws

There may still be errors around that the developers might not have noticed. These errors might still give some useful information to hackers. And if the errors are correctly handled, but the error messages are too informational, the hacker might still reason what might be happening behind the scenes. If the errors aren't handled properly the use might also be the victim, because it becomes difficult to use the application if you cannot see what goes wrong.

## Cases

- [Airquality](cases/airquality#Vulnerabilities)

If there's an error, the error messages display very little to no information. This is very inconvenient to both the user and the developer because nobody can see what went wrong.

- [Smartscreen](cases/smartscreen#Vulnerabilities)

The Smartscreen had no problem with error handling.

- [Smartwatch](cases/smartwatch#Vulnerabilities)

Not Applicable.

## Bibliography

[Owasp Error Handling](https://owasp.org/www-community/Improper_Error_Handling)
