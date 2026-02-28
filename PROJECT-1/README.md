# Artemis Financial Vulnerability Assessment
## Project Overview

Artemis Financial is a company that develops software used to manage financial plans and sensitive client information. Because their application handles personally identifiable and financial data, secure communication and data protection are critical requirements.

The company needed a vulnerability assessment of its REST-based application to identify security risks and recommend improvements. The main concern was protecting client data during transmission and preventing common web-based threats such as injection attacks or interception of API traffic.

## What I Identified

Through manual review of the codebase, I identified several security risks that could expose the system to misuse or unauthorized access.

### Key findings included:

User input accepted and reflected without validation

API endpoints mapped too broadly, increasing attack surface

Hardcoded database credentials stored in source code

Stack trace logging that could reveal internal system details

Financial data being modified without proper validation

Because this application is built on a REST API, these issues are especially important since APIs are a common attack surface and often exposed to external users.

## Why Secure Coding Matters

Secure coding is essential for financial platforms because even small vulnerabilities can lead to data exposure, manipulation, or loss of trust.

By identifying weaknesses such as unvalidated inputs and improper credential handling, this assessment demonstrated how security flaws can exist even in functional systems.

Improving software security adds real business value by:

Protecting client data

Preventing unauthorized system access

Reducing regulatory and reputational risk

Supporting long-term system reliability

## Challenges and Learning Experience

One of the most challenging parts of this project was translating security theory into practical code-level issues.

It required looking beyond whether the software worked and instead asking:

*Could this behavior be exploited?*

The manual review process was especially useful because it highlighted how small design choices, like reflecting user input or logging stack traces, can introduce real vulnerabilities if not handled properly.

## Security Improvements

To strengthen the application, I recommended several mitigation steps:

Adding input validation across REST endpoints

Restricting API mappings to required HTTP methods only

Moving database credentials out of source code

Replacing stack trace printing with controlled logging

Validating financial transaction inputs

Updating vulnerable dependencies identified during static testing

Static analysis also revealed multiple outdated libraries with known vulnerabilities, including components in Spring, Jackson, Tomcat, and SnakeYAML, reinforcing the importance of dependency management in secure development.

## Ensuring Functionality and Security

Security improvements must not break functionality.

After identifying vulnerabilities, the focus was on recommending changes that would:

Maintain application behavior

Reduce attack surface

Improve protection of sensitive data

Balancing usability and security is a key part of real-world software development.

## Tools and Practices Used

This project reinforced several practices that will carry forward into future work:

Manual vulnerability review

Dependency risk analysis

REST API security considerations

Secure credential handling

Input validation strategies

These approaches help ensure that applications are not only functional but also resilient against common threats.

## Portfolio Value

From this project, I can demonstrate to future employers:

Ability to identify real software vulnerabilities

Understanding of REST API security risks

Experience performing manual security reviews

Awareness of dependency-based threats

Practical knowledge of mitigation strategies

This work reflects the ability to evaluate an existing system and recommend realistic steps to improve its security posture.
