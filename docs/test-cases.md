---
layout: default
title: Test Cases
nav_order: 3
---

{: .important-title }
> Login User Story
>
> Website: https://www.saucedemo.com
>
> Rule:
>
> Accepted usernames are: standard_user, locked_out_user, problem_user, performance_glitch_user
>
> Password for all users: secret_sauce

[View Test Case](https://docs.google.com/spreadsheets/d/1HE1bMMztXkqoShD0vNOh_FE6va96WYkIiDsquOLHhCY/edit?usp=sharing){: .btn .btn-outline }

![](/assets/images/google-sheet-test-case.png)

## BDD Test Case

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

  Scenario #2: User login failed with incorrect username and password
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

## Qase Test Case

User successfully logged in with correct username and password

Steps to reproduce:

![](/assets/images/qase-test-case.png)
