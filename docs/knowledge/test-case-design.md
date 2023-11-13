---
layout: default
title: Test Case Design
parent: Knowledge
nav_order: 7
---

{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
- TOC
{:toc}
</details>

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

**Understand the requirements**:

The first step is to thoroughly understand the requirements you are testing. This means reading the requirements document carefully and asking any clarifying questions you have.

For example, if the requirement is "Users must be able to log in to the system using their username and password.", you should ask questions like:

* What is a valid username and password?
* What happens if a user enters an invalid username or password?
* How many times can a user try to log in before being locked out?

**Identify different types of requirements**:

There are different types of requirements, such as functional requirements, non-functional requirements, and acceptance criteria. Functional requirements describe what the system should do, while non-functional requirements describe how the system should function. Acceptance criteria are specific conditions that must be met for a requirement to be considered fulfilled.

For example, a functional requirement for a login system might be: "Users must be able to log in to the system using their username and password.", while a non-functional requirement might be : "The login system must be able to handle 100 concurrent users."

**Prioritize requirements**:

Not all requests are created equal. Some requirements are more important than others. By clarifying requirements, you can focus your efforts on the most important requirements.

For example, requiring that users be able to log in to the system is more important than requiring that the login system be able to handle 100 concurrent users. This is because users will not be able to use the system if they cannot log in.

## Design with BDD approach

1. **Understand the Feature:**
   - Before writing BDD test cases, make sure you have a thorough understanding of the feature or user story you are testing. Collaborate with stakeholders to clarify requirements.

2. **Use "Given-When-Then" Structure:**
   - Follow the "Given-When-Then" (GWT) structure for writing scenarios. Clearly state the initial context ("Given"), the action or event ("When"), and the expected outcome ("Then").

3. **Write Descriptive Scenarios:**
   - Use descriptive and meaningful language in your scenarios. Clearly communicate the intended behavior to anyone reading the scenario, including non-technical stakeholders.

4. **Be Specific:**
   - Provide specific details in your scenarios. Avoid ambiguity and use concrete examples to illustrate the expected behavior. Specificity helps in test execution and understanding.

5. **Keep Scenarios Short and Focused:**
   - Write scenarios that are concise and focused on a single aspect of the feature. This makes it easier to understand, maintain, and troubleshoot.

6. **Avoid Technical Details:**
   - BDD scenarios should focus on the behavior from a user's perspective. Avoid unnecessary technical details in your scenarios, as they can make the scenarios less accessible to non-technical team members.

7. **Utilize Background:**
   - Use the Background section in your feature file to set up the initial context that is common to multiple scenarios. This reduces repetition and enhances readability.

8. **Use Scenario Outline for Data Variations:**
   - If your scenario involves multiple sets of data, use the Scenario Outline keyword. This allows you to write a scenario template and provide different data sets for testing variations.

    ```plaintext
    Scenario Outline: User Authentication
      Given a user is on the login page
      When they enter <username> and <password>
      Then they should be <authentication_result>

    Examples:
      | username | password | authentication_result |
      | valid    | secret   | successfully logged in  |
      | invalid  | wrong    | login failed            |
    ```

9. **Include Negative Scenarios:**
   - Cover negative scenarios to test how the system handles errors or invalid inputs. This ensures a more robust testing approach.

10. **Use Tags for Organization:**
    - Tag scenarios with relevant keywords to categorize them. Tags can include aspects such as priority, functionality, or the type of test (e.g., @smoke, @regression).

11. **Review and Refine:**
    - Regularly review and refine your BDD scenarios. Update them to reflect changes in requirements or the system's behavior. Keep scenarios aligned with the evolving application.

12. **Collaborate with the Team:**
    - Involve team members, including developers, testers, and product owners, in the creation and review of BDD scenarios. Collaboration ensures a shared understanding of the desired behavior.

13. **Document Assumptions:**
    - If your scenario relies on specific assumptions, document them. This helps team members understand the context and ensures that everyone is on the same page.

14. **Use Clear and Meaningful Names:**
    - Choose clear and meaningful names for your feature files, scenarios, and steps. This enhances readability and makes it easier to locate and understand specific test cases.

By following these principles, you can create BDD test cases that are not only effective in verifying the behavior of your software, but also serve as clear documentation for your project. And to understand more about BDD, you can see more articles on [this topic here](https://namnh663.github.io/docs/knowledge/behavior-driven-development.html)