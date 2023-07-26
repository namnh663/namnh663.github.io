---
layout: default
title: Test Cases
nav_order: 3
---

## BDD Test Case

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

Login Test Case:

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
