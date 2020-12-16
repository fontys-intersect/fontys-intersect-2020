# Error Handling

This page will go in-depth on the topic of error handling; what it is, why it's important, and how it could be implemented securely.

## Table of Contents

- [Explanation](#explanation)
- [Uses](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

Error handling is important for running a smooth application. It is used in any code, from applications to backends and other software. Good error handling goes hand in hand with good testing. The tests are very important as well since it will show how well the error handling is implemented.

## Usage

If anything unexpected happens, either on the client-side or the server-side, the error will be caught and handled internally. The user will see a basic message what might have gone wrong without giving out too much information. If there are any unhandled errors and the website crashes or not work as intended. A good rule of thumb is that if it is a client-side error show as much information as possible and if it is a server-side error, leak as little information as possible, as recommended by the [IOT Security Foundation Guidelines, 2019](https://www.iotsecurityfoundation.org/wp-content/uploads/2019/12/Best-Practice-Guides-Release-2_Digitalv3.pdf).

## Flaws

There may still be errors around that the developers might not have noticed. These errors might still give some useful information to hackers. And if the errors are correctly handled, but the error messages are too informational, the hacker might still reason what might be happening behind the scenes. If the errors aren't handled properly the use might also be the victim, because it becomes difficult to use the application if you cannot see what goes wrong.

### Owasp

For more information, the [Owasp Error Handling](https://owasp.org/www-community/Improper_Error_Handling) page has more, in-depth guidelines to what to do with error handling and how to implement it.

## Cases

- [Airquality](cases/airquality#Vulnerabilities)

If there's an error, the error messages display very little to no information. This is very inconvenient to both the user and the developer because nobody can see what went wrong.

- [Smartscreen](cases/smartscreen#Vulnerabilities)

The Smartscreen had no problem with error handling.

- [Smartwatch](cases/smartwatch#Vulnerabilities)

Not Applicable.

## Bibliography

- [IOT Security Foundation Guidelines, 2019](https://www.iotsecurityfoundation.org/wp-content/uploads/2019/12/Best-Practice-Guides-Release-2_Digitalv3.pdf)
- [Owasp Error Handling](https://owasp.org/www-community/Improper_Error_Handling)
