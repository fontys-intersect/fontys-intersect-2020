# Splict Development and Production Environments

An in-depth page about splitting development and production environments. In this page, it will be explained how it works and how it could be implemented.

## Table of Contents
- [Splict Development and Production Environments](#splict-development-and-production-environments)
  - [Table of Contents](#table-of-contents)
  - [Explanation](#explanation)
  - [Uses](#uses)
  - [Flaws](#flaws)
  - [Cases](#cases)
  - [Bibliography](#bibliography)
  - [Appendix](#appendix)

## Explanation 
When you deveop products, it will go through several steps. From developing, testing, to eventual production. All of these stages need an environment and something that ties them all together, like a pipeline. 

## Uses
A good practice is to create seperate server environments for development, test, staging and production. Every development lifecycle should maintain at least two server environments for production and everything else. This will provide separetion between custumer's systems and those that should not be publicly exposed. 

## Flaws
If you are a small company with little resources, you might not be able to achieve a true split. In that case, instead of splitting every single step, split it into development and production. In development, use version management and test. 

## Cases
The cases that are relevant to this best practice

## Bibliography
All sources used for thie specific subject. 

## Appendix
Any extra pages about this subject.