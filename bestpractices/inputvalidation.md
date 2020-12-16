# Input Validation

Every users input should be properly validated, to make sure that nothing malicous is entered.

## Table of Contents

- [Input Validation](#input-validation)
  - [Table of Contents](#table-of-contents)
  - [Explanation](#explanation)
  - [Usage](#usage)
  - [Flaws](#flaws)
  - [Cases](#cases)
  - [Bibliography](#bibliography)

## Explanation

Input validation is making sure that what you enter in a text field is what you're supposed to enter. E-mails, for example, should be written as user@example.com, and not just any string.

## Usage

**Taking Advantage**
Input validation, on both the frontend and the backend, is important. If the program expects a certain value or string, it should get that value or string. If it gets something unexpected, and it's handled incorrectly, the program or website could crash. Hackers might also take advantage of bad input validation, like entering negative values in a money transfer, effectively giving themselves the money. It is also useful to avoid a textbox-based attack, like SQL-injection and cross-site scripting (XSS).

**Checks**
There are several ways to validate inputs. Minimum and maximum range checks, type converters, and regex are some ways to do so. Some frameworks have it built-in, like Django or Angular. There are also JSON or XML schemas to check inputs against. Besides text input validation other inputs such as files should also be checked. This can be done by limiting the accepted file types. According to Nist(2020) input validation errors should be reviewed and resolved within a predefined time period.

**Manual override**
Nist(2020) recommends to add manual override capabilities for input validation. The access to this override should be restricted to only be accessible to organization-defined authorized individuals. "In certain situations, such as during events that are defined in contingency plans, a manual override capability for input validation may be needed"(Nist, 2020) the use of the manual override should be limited.

**Functions**
Certain functions should not be used with unchecked user input, because an attacker could be able to inject dangerous input into the function. Always read the documentation carefully to make sure that you do not make any mistakes. Most proper frameworks have solutions for these problems, but they must be used correctly in order to work.

## Flaws

If the input validation is only in the front-end but not in the backend, hackers may send crafted requests with messages that would not have been accepted by the frontend. Make sure to implement the validation in the backend. All frontend checks can be circumvented by a simple proxy, so checking the backend is crucial.

Lastly, it is better to whitelist than to blacklist certain characters or strings. If you try to blacklist `<script>` or `1=1` you might end up with an exploit anyway because hackers found a way to evade this. Whitelisting will tell the website what is authorized, and by default, anything else won't be authorized.

## Cases

- [Airquality](cases/airquality#Vulnerabilities)

An attacker can omit certain parameters when making new users, sensors or locations, making these invalid.

## Bibliography

- [OWASP](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html)
- [Security and Privacy Controls for Information Systems and Organizations, Nist, December 10 2020.](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
