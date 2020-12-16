# Split Development and Production Environments

When developing a system, the developers use tools to make it easier. These tools and options should be removed before shipping everything to production, since these tools can be abused.

## Table of Contents

- [Split Development and Production Environments](#split-development-and-production-environments)
- [Table of Contents](#table-of-contents)
- [Explanation](#explanation)
- [Uses](#uses)
- [Flaws](#flaws)
- [Cases](#cases)
- [Bibliography](#bibliography)

## Explanation

When you develop a product, it will go through several steps. From developing, testing, to eventual production. All of these stages need an environment and something that ties them all together, like a pipeline. These environments need to be different so that there is nothing left over from testing in production.

## Uses

A good practice is to create separate server environments for development, test, staging and production. Every development lifecycle should maintain at least two server environments, for production and everything else. This will provide separation between the customer's systems and those that should not be publicly exposed.

## Flaws

If you are a small company with little resources, it might be hard to achieve a true split. In that case, instead of splitting every single step, split it into development and production. In development, use version management and test. Production is what is exposed to the outside, this should contain no remains of testing. A big problem is that systems confuse these and test in production. This can leave very big security risks, such as the ADB in the smart screen case.

## Cases

During the pentests that we performed, we found this security issue in two of the products that we tested.

- [Smartscreen](cases/smartscreen#Vulnerabilities)
  
It was found that one of the Smart Screens had a debugging panel open which is meant for a development environment.

- [Airquality](cases/airquality#Vulnerabilities)

The other case was with the airquality, where the project was building a development version, and pushing it to production.

## Bibliography

Not Applicable
