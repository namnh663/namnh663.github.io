---
layout: default
title: Bugs
nav_order: 3
---

## Bug Report

**Context**: I get an error when I use a valid account to login, but I get the message that my account has been locked while I have never logged in wrong and no one is using my account to log in system

Let's assume I use Jira to create Bug

1. Press keyboard shortcut C
2. Show Create issue popup
3. Select Issue type = Bug
4. Fill in the fields:
   1. Summary: The account is not locked but can't log in
   2. Root cause: Code
   3. Priority: Medium
   4. Environment: Test
   5. Platform: Web
   6. Browser: Chrome
   7. Description:
      1. Given user go to 'https://www.saucedemo.com/'
      2. When user enter 'standard_user' to username textbox
      3. And user enter 'secret_sauce' to password textbox
      4. And user click Login button
      5. Then user see 'Epic sadface: Sorry, this user has been locked out.' error message
      6. And should attach actual error image

         **Expcted**: User should go to home page
   8. Assignee: Andrew
   9. Reporter: Me
   10. Sprint: Swag Labs Sprint 1
5. Click Create

## Workflow

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
