---
layout: default
title: About
nav_order: 1
description: "Portforlio"
permalink: /
---

**Address**: Ho Chi Minh, Vietnam | **Email**: namnh663@gmail.com | **Mobile**: 086 909 1664
{: .fs-6 .fw-300 }

[GitHub](https://github.com/namnh663){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[LinkedIn](https://www.linkedin.com/in/namnh663){: .btn .fs-5 .mb-4 .mb-md-0 }

### About Me

- 5 years of experience in software testing
- Familiar with manual testing and automation roles
- Proficient in different testing methods and test planning
- Proficient in web and mobile testing
- Experienced in leading a small team
- Strong skills attention to detail
- Excellent at collaborating with teams and working closely
- Very serious and straightforward when working
- Love to share and learn new technologies and trends in the software testing industry

### Skills

- Familiar with software development life cycle (SDLC) models, software testing life cycle (STLC), bug life cycle
- Scrum insight - an agile project management framework
- Proficient use of Jira Board, Jira Timeline, Jira Reports, Jira Backlog, Jira Automation, Jira Filters, Jira Dashboards
- Proficient use of Azure DevOps, Azure Pipelines, Azure Boards, Azure Repos, Azure Test Plans, Azure Load Testing, Azure Monitor - Application Insights
- Experienced in writing test documents
- Requirement / User story analysis
- Proficient in creating and executing test cases
- Bug report
- Regression Testing
- Agile Testing
- API Testing
- Functional Testing
  - Integration Testing
  - System Testing: Blackbox, E2E, Smoke
  - Acceptance Testing
- Non-Functional Testing
  - Performance Testing
  - Usability Testing: Exploratory, Browser
- Performing demo sessions
- Experienced in implementing test automation framework from scratch

### Some Examples

#### BDD Test Case

Website: https://www.saucedemo.com/

Requirement:
- Accepted usernames are: standard_user, locked_out_user, problem_user, performance_glitch_user
- Password for all users: secret_sauce

Check List:
1. Display all the elements of the login page and the UI must be the same as the design
2. Default username and password are empty
3. Default username field's placeholder is Username
4. Default password field's placeholder is Password
5. Username and password are blank on page reload
6. User successfully logged in with correct username and password
7. User login failed with incorrect username and password
8. User login failed with correct name but incorrect password
9. User login failed with incorrect name but correct password
10. User login failed when username and password are left blank
11. User login failed when entering username but leaving password blank
12. User login failed when name is left blank but password is entered
13. Error message appears above login button and does not close automatically

```
Feature: Login
  As a new user
  I want to log in to the website 
  So that the system can remember my data

  Scenario #1: User successfully logged in with correct username and password
    Given user go to 'https://www.saucedemo.com/'
    When user enter 'standard_user' to username textbox
    And user enter 'secret_sauce' to password textbox
    And user click Login button
    Then user should be successfully logged into the site

  Scenario #2: User login failed when username and password are left blank
    Given user go to 'https://www.saucedemo.com/'
    Then user should see the username field blank
    And user should see the password field blank
    When user click Login button
    Then user should see the username field highlighted in red
    And user should see the password field highlighted in red
    And user should see 'Epic sadface: Username is required' error message

  Scenario #3: User login failed with incorrect username and password
    Given user go to 'https://www.saucedemo.com/'
    When user enter <invalid_username> to username textbox
    And user enter <invalid_password> to password textbox
    And user click Login button
    Then user should see 'Epic sadface: Username and password do not match any user in this service' error message

    Examples: Account
        | invalid_username | invalid_password |
        | standard_userrrr | secret_sauceeeee |
        | standardUserrrrr | secretSauceeeeee |
        | standardUserrr12 | secretsAuceeeee0 |
        | standard@userrrr | !@#9875sauceeeee |
        | 1212121242344545 | !e45645645645677 |
        | STANDARD_USER    | SECRET_SAUCE     |
```

#### Bug

**Context**: I get an error when I use a valid account to login, but I get the message that my account has been locked while I have never logged in wrong and no one is using my account to log in system

Let's assume I use Jira to create bug

1. Press keyboard shortcut C
2. Show Create issue popup
3. Select Issue type = Bug
4. Fill in the fields:
   1. Summary: The account is not locked but can't log in
   2. Root cause: Code
   3. Priority: Medium
   4. Environment: Test
   5. Description:
      1. Given user go to 'https://www.saucedemo.com/'
      2. When user enter 'standard_user' to username textbox
      3. And user enter 'secret_sauce' to password textbox
      4. And user click Login button
      5. Then user see 'Epic sadface: Sorry, this user has been locked out.' error message
      6. And should attach actual error image

         **Expcted**: User should go to home page
   7. Assignee: Andrew
   8. Sprint: Swag Labs Sprint 1
5. Click Create

**Workflow**:

Blocked: Any status to move to this status

Done: Any status to move to this status

| **Transition** | **From status** | **Transition** | **To status** |
| --- | --- | --- | --- |
| Create | Open | ➜ | Handover |
|  | Handover | ➜ | In Dev |
|  | Handover | ➜ | Won't Fix |
|  | In Dev | ➜ | Ready For QA |
|  | Ready For QA | ➜ | In Test |
|  | In Test | ➜ | Reopened |
|  | Reopened | ➜ | In Dev |
