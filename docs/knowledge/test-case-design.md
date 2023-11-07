---
layout: default
title: Test Case Design
parent: Knowledge
nav_order: 6
---

# Test Case Design

To design effective test cases, you need to follow a few key steps:

1. **Identify the test objectives:** What do you want to test? What functionality or behavior are you trying to verify?
2. **Analyze the requirements:** What are the functional, non-functional, and integration requirements for the system or feature you are testing?
3. **Design test scenarios:** These are high-level descriptions of the different ways that the system can be used and the different types of inputs and outputs that are possible.
4. **Derive test cases:** Each test case should be a specific instance of a test scenario. It should include the following information:
    * Test case ID
    * Test case name
    * Preconditions (the state of the system before the test case is executed)
    * Test steps
    * Test data
    * Expected result
    * Actual result
    * Status

Sample example: [Template](https://namnh663.github.io/docs/document.html#test-case)

Here are some best practices for designing effective test cases:

* **Focus on user requirements:** Make sure that your test cases cover all of the critical aspects of the application that users will be interacting with.
* **Keep test cases simple and concise:** Each test case should focus on a single test objective. Avoid creating test cases that are too complex or that test multiple things at once.
* **Cover both positive and negative scenarios:** Positive testing verifies that the system works as expected when given valid inputs. Negative testing verifies that the system handles invalid or unexpected inputs gracefully.
* **Use boundary value analysis and equivalence partitioning:** Boundary value analysis tests the system at the edges of its input domain. Equivalence partitioning divides the input domain into equivalence classes, and then tests one test case from each equivalence class.
* **Use a consistent format and structure for test cases:** This will make them easier to read, understand, and maintain.

Once you have designed your test cases, you should review them with other team members to get feedback. This will help to ensure that your test cases are comprehensive and effective.

## Analyze the requirements

1. Understand the requirements

The first step is to thoroughly understand the requirements you are testing. This means reading the requirements document carefully and asking any clarifying questions you have.

For example, if the requirement is "Users must be able to log in to the system using their username and password.", you should ask questions like:

* What is a valid username and password?
* What happens if a user enters an invalid username or password?
* How many times can a user try to log in before being locked out?

2. Identify different types of requirements

There are different types of requirements, such as functional requirements, non-functional requirements, and acceptance criteria. Functional requirements describe what the system should do, while non-functional requirements describe how the system should function. Acceptance criteria are specific conditions that must be met for a requirement to be considered fulfilled.

For example, a functional requirement for a login system might be: "Users must be able to log in to the system using their username and password.", while a non-functional requirement might be : "The login system must be able to handle 100 concurrent users."

3. Prioritize requirements

Not all requests are created equal. Some requirements are more important than others. By clarifying requirements, you can focus your efforts on the most important requirements.

For example, requiring that users be able to log in to the system is more important than requiring that the login system be able to handle 100 concurrent users. This is because users will not be able to use the system if they cannot log in.