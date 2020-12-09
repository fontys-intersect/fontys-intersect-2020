# Input Validation

An in-depth page about the Input Validation. In this page, it will be explained how it works and how it could be implemented.

### Table of Contents

- [Explanation](#explanation)
- [Uses](#usage)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

Input validation is making sure that what you enter in a text field is what you're supposed to enter. E-mails, for example, should be written as user@example.com, and not just any string.

## Usage

**Taking Advantage**
Input validation, on both frontend and the backend, is important. If the program expects a certain value or string, it should get that value or string. If it gets something unexpected, and it's handled incorrectly, the program or website could crash. Hackers might also take advantage of bad input validation, like entering negative values in a money transfer, effectively giving themselves the money. It is also useful to avoid a textbox-based attack, like SQL-injection and cross-site scripting (XSS).

**Checks**
There are several ways to validate inputs. Minimum and maximum range checks, type converters, and regex are some ways to do so. Some frameworks have it built-in, like Django or Angular. There are also JSON or XML schemas to check inputs against.

## Flaws

If the input validation is only in the front-end but not in the backend, hackers may send crafted requests with messages that would not have been accepted by the frontend. Make sure to implement the validation in the backend. All frontend checks can be circumvented by a simple proxy, so checking the backend is crucial.

Lastly, it is better to whitelist than to blacklist certain characters or strings. If you try to blacklist `<script>` or `1=1` you might end up with XSS anyway because hackers found a way to evade this. Whitelisting will tell the website what is authorized, and by default, anything else won't be authorized.

## Cases

%TODO%

## Bibliography

- [OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html)