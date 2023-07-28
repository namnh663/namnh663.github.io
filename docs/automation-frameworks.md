---
layout: default
title: Automation Frameworks
nav_order: 5
---

## Familiar With Automation Testing Frameworks

| Frameworks        | Post On LinkedIn          |
|:------------------|:--------------|
| <img src="https://raw.githubusercontent.com/DevExpress/testcafe-gh-page-assets/master/src/images/testcafe-ogp-icon.png" width="150" height="75">                | [TestCafe](https://www.linkedin.com/posts/namnh663_testing-testcafe-automation-activity-7005242655332855808-VDc9?utm_source=share&utm_medium=member_desktop)|
| <img src="https://www.lambdatest.com/resources/images/header/Playwright_logo.svg" width="150" height="75">                | [Playwright](https://www.linkedin.com/posts/namnh663_testing-automation-framework-activity-6995858645141901312-Gjgx?utm_source=share&utm_medium=member_desktop)|
| <img src="https://repository-images.githubusercontent.com/81226206/2392b041-2ddb-438c-91ae-4022cf7f4549" width="150" height="75">                | [Karate](https://www.linkedin.com/posts/namnh663_testing-automation-framework-activity-6991862237917327360-aMfZ?utm_source=share&utm_medium=member_desktop)|
| <img src="https://icehousecorp.com/wp-content/uploads/2022/07/robot-f.png" width="150" height="75">                | [Robot](https://www.linkedin.com/posts/namnh663_testing-robotframework-automation-activity-7088958406123814912-VKdG?utm_source=share&utm_medium=member_desktop)|

### Robot Framework

#### Structure

```
📦 
.gitignore
├─ .vscode
settings.json
├─ data
│  ├─ messages.py
│  └─ users.py
readme.md
resources
│  ├─ page-objects
│  │  ├─ elements
│  │  │  ├─ cart_elements.py
│  │  │  ├─ login_elements.py
│  │  │  └─ products_elements.py
│  │  └─ keywords
│  │     ├─ cart_page.robot
│  │     ├─ login_page.robot
│  │     └─ products_page.robot
│  └─ utils
│     └─ custom_keywords.py
├─ results
│  ├─ log.html
│  ├─ output.xml
│  └─ report.html
└─ tests
   ├─ e2e
   │  └─ checkout.robot
   └─ functional
      ├─ authentication
      │  ├─ access_link.robot
      │  └─ login.robot
      └─ cart
         ├─ add_item.robot
         └─ display.robot
```

#### Login Script

```
*** Settings ***
Resource            ../resources/page-objects/keywords/login_page.robot
Resource            ../resources/page-objects/keywords/products_page.robot

Test Setup          login_page.Open Browser To Login Page
Test Teardown       Close Browser

Name                Login Tests


*** Test Cases ***
Valid Login
    [Documentation]    Valid Login
    [Tags]    functional
    login_page.Input Username    ${USER_001}
    login_page.Input Password    ${PASSWORD_COMMON}
    login_page.Submit Credentials
    products_page.Products Page Should Be Open And Title Should Be    Swag Labs

Empty Username And Password
    [Documentation]    Invalid Login When Username And Password Are Empty
    [Tags]    functional
    login_page.Input Username    ${EMPTY}
    login_page.Input Password    ${EMPTY}
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_001}

Empty Username
    [Documentation]    Invalid Login When Empty Username
    [Tags]    functional
    login_page.Input Username    ${EMPTY}
    login_page.Input Password    ${PASSWORD_COMMON}
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_001}

Empty Password
    [Documentation]    Invalid Login When Empty Password
    [Tags]    functional
    login_page.Input Username    ${USER_001}
    login_page.Input Password    ${EMPTY}
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_002}

Invalid Username
    [Documentation]    Invalid Login When Invalid Username
    [Tags]    functional
    login_page.Input Random Username
    login_page.Input Password    ${PASSWORD_COMMON}
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_003}

Invalid Password
    [Documentation]    Invalid Login When Invalid Password
    [Tags]    functional
    login_page.Input Username    ${USER_001}
    login_page.Input Random Password
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_003}

Invalid Username And Password
    [Documentation]    Invalid Login When Invalid Username And Password
    [Tags]    functional
    login_page.Input Random Username
    login_page.Input Random Password
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_003}

Locked Account
    [Documentation]    Invalid Login When Current User Has Been Locked
    [Tags]    functional
    login_page.Input Username    ${USER_002}
    login_page.Input Password    ${PASSWORD_COMMON}
    login_page.Submit Credentials
    login_page.Error Message Should Be    ${LOGIN_ERROR_MSG_004}
```
