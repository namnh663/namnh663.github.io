---
layout: default
title: Bugs
nav_order: 4
---

## Bug Report

{: .important-title }
> Context
>
> I get an error when I use a valid account to login, but I get the message that my account has been locked while I have never logged in wrong and no one is using my account to log in system

Let's assume I use Jira to create Bug

1. Press keyboard shortcut C
2. Show Create issue popup
3. Select Issue type = Bug
4. Fill in the fields:
   
   | Fields | Value |
   | --- | --- |
   | Summary | The account is not locked but can't log in |
   | Root cause | Code |
   | Priority | Medium |
   | Environment | Test |
   | Platform | Web |
   | Browser | Chrome |
   | Description | Given user go to 'https://www.saucedemo.com/'<br>When user enter 'standard_user' to username textbox<br>And user enter 'secret_sauce' to password textbox<br>And user click Login button<br>Then user see 'Epic sadface: Sorry, this user has been locked out.' error message<br>**Expected**:  User should go to home page |
   | Related Issues | Login User Story |
   | Assignee | Andrew |
   | Reporter | Me |
   | Sprint | Sprint 1 |
   
6. Click Create

## Workflow

Blocked: Any status to move to this status

Done: Any status to move to this status

| Transition | From status | Transition | To status |
|:-----------|:------------|:-----------|:----------|
| Create | Open | ➜ | Handover |
|  | Handover | ➜ | In Dev |
|  | Handover | ➜ | Won't Fix |
|  | In Dev | ➜ | Ready For QA |
|  | Ready For QA | ➜ | In Test |
|  | In Test | ➜ | Reopened |
|  | Reopened | ➜ | In Dev |
