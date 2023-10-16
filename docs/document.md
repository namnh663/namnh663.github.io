---
layout: default
title: Document
nav_order: 3
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

# Template

## User Story

Logging in to www.saucedemo.com

**As** a registered user of www.saucedemo.com,

**I want to** log in to my account,

**So that I can** make purchases on the website.

**Acceptance Criteria:**

1. **Given** I am on the www.saucedemo.com homepage,

   **When** I click on the "Login" button,

   **Then** I should be redirected to the login page.

2. **Given** I am on the login page,

   **When** I enter my valid username and password,

   **Then** I should see a confirmation message, and I should be logged in to my account.

3. **Given** I am on the login page,

   **When** I enter an invalid username or password,

   **Then** I should see an error message indicating that my login credentials are incorrect.

4. **Given** I am logged in,

   **When** I browse the website and select products,

   **Then** I should be able to add products to my cart and proceed with the checkout process.

5. **Given** I am logged out of my account,

   **When** I click the "Log Out" button,

   **Then** I should be logged out and redirected to the homepage.

**Definition of Done:**

- The user can successfully log in to their account.
- The user can browse and add products to their cart.
- The user receives appropriate feedback for login success or failure.
- The "Log Out" functionality is working as expected.


## Test Plan

**1. Introduction**

   - **Website Under Test**: www.saucedemo.com
   - **Test Objective**: To ensure the functionality, usability, and security of the website.
   - **Test Environment**: Specify the browsers, devices, and operating systems to be tested on.

**2. Scope**

   - Identify the features, functional or non-functional requirements of the website that will be tested:
     - Login functionality
     - Product catalog
     - Shopping cart
     - Checkout process
     - User account management
   - Specify any features or functionalities that are out of scope:
     - Mobile responsiveness
     - Security testing
     - Performance testing
     - Compatibility testing

**3. Test Objectives**

   - Validate the website's functionality according to its specifications.
   - Ensure the website is user-friendly and easy to navigate.
   - Verify the website's security against common vulnerabilities.
   - Assess the website's performance and scalability.
   - Confirm cross-browser compatibility.

**4. Test Cases**
   
   [View Test Case](https://docs.google.com/spreadsheets/d/1HE1bMMztXkqoShD0vNOh_FE6va96WYkIiDsquOLHhCY/edit?usp=sharing){: .btn .btn-outline }

**5. Test Data**

   - Username:
     - standard_user · locked_out_user · problem_user · performance_glitch_user
   - Password: 
     - secret_sauce

**6. Test Execution**

**Testing Team:**

   | # | Role          | Member |
   |:--|:--------------|:-------|
   | 1 | QA Lead       | Nam    |
   | 2 | Senior Tester | Trang  |
   | 3 | Junior Tester | Tri    |
   | 4 | Intern        | Phu    |
   | 5 | Intern        | Han    |

**Test Schedule:**

   - Test Phase 1 (Login and Navigation):
     - Start Date: [Insert Start Date]
     - End Date: [Insert End Date]

   - Test Phase 2 (Shopping and Checkout):
     - Start Date: [Insert Start Date]
     - End Date: [Insert End Date]

   - Test Phase 3 (User Account and Security):
     - Start Date: [Insert Start Date]
     - End Date: [Insert End Date]

**Test Case Execution**

   - Execute the test cases, logging any defects found during testing.

**7. Defect Management:**

   - Define the process for reporting, tracking, and prioritizing defects.
   - Assign responsibilities for defect resolution.

**8. Test Environments:**

   - Describe the test environments, including the hardware, software, and network configurations used for testing.

**9. Risks and Assumptions:**

**Example 1**:
   - Risk ID: RSK001
   - Description: Network Connectivity Issues
   - Probability: Moderate
   - Impact: High
   - Mitigation Plan: Ensure that the testing environment has a stable internet connection and a backup plan for testing in case of connectivity issues.

**Example 2**:
   - Risk ID: RSK002
   - Description: Unavailability of Test Data
   - Probability: Low
   - Impact: Moderate
   - Mitigation Plan: Prepare a backup set of test data in case the primary test data becomes unavailable or corrupted.

**10. Deliverables:**
    - Specify the test documentation to be delivered, such as test reports, defect reports, and test data.

**11. Exit Criteria:**

**Functional Testing**:
   - **Criteria:** All critical and high-priority functional test cases have been executed, and no critical defects are outstanding.
   - **Example:** All login-related test cases have been executed, and no critical defects are open. There are no high-priority defects affecting the login, product catalog, shopping cart, or checkout functionalities.

**Usability Testing**:
   - **Criteria:** Usability testing has been conducted, and user feedback has been analyzed to ensure that the website is user-friendly.
   - **Example:** Usability tests were conducted with a sample group of users, and their feedback has been collected and analyzed. Necessary improvements have been made based on the feedback, and user satisfaction has increased.

**Regression Testing**:
   - **Criteria:** Regression testing has been performed, and no new defects have been introduced as a result of recent changes.
   - **Example:** After implementing updates to the website, a full regression test was conducted, and no new defects were identified. Any previously fixed defects remained resolved.

**Test Documentation**:
   - **Criteria:** All required test documentation, including test cases, test reports, and defect reports, have been completed and reviewed.
   - **Example:** Test cases for all identified functionalities have been documented, test execution reports have been generated and reviewed, and all defects have been documented with clear steps to reproduce.

**Stakeholder Approval**:
   - **Criteria:** Stakeholders, including the project manager and product owner, have reviewed and approved the test results and are satisfied with the quality of the website.
   - **Example:** The project manager and product owner have reviewed the test reports, participated in user acceptance testing, and have provided their formal approval for the website to move to production.

**12. Resources:**
   - List the resources needed for testing, including personnel, tools, and hardware.

**13. Approval:**
   - Identify the stakeholders responsible for approving the test plan.

**14. Review and Update:**
   - Specify when and how the test plan will be reviewed and updated throughout the testing process.

**15. Conclusion:**
   - Summarize the test plan and its key objectives.

## Test Case

### Google Sheet Test Case

![](/assets/images/google-sheet-test-case.png)

[View Test Case](https://docs.google.com/spreadsheets/d/1HE1bMMztXkqoShD0vNOh_FE6va96WYkIiDsquOLHhCY/edit?usp=sharing){: .btn .btn-outline }

### BDD Test Case

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

### Qase Test Case

User successfully logged in with correct username and password

Steps to reproduce:

![](/assets/images/qase-test-case.png)


## Bug Report

[View Bug Report](https://swaglabs.almanac.io/docs/bug-report-template-9sBBi1stle8PHVQezELGfdhc0QXmBs6D){: .btn .btn-outline }

# Database

## DbGate

### Connection

```
-- Sever
103.191.146.31
-- Port
23307
-- User
dev1_qc /  dev2_qc / devIntegrate_qc
-- Password
TSC4qP1tmbXRok6UmaqN /  EAqlm6fiDvCUBV23YX0M /  XSQsuNb0H7ulnuwiPFiZ
```

### Query

```sql
-- Drop foreign key DTTariffMainItems
ALTER TABLE `DTTariffMainItems` DROP FOREIGN KEY `FK_DTTariffMainItems_DTTariffMains_TariffId`;
-- Drop foreign key DTTariffVASItems
ALTER TABLE `DTTariffVASItems` DROP FOREIGN KEY `FK_DTTariffVASItems_DTTariffVASs_TariffId`;
-- Drop foreign key FMTariffMainItems
ALTER TABLE `FMTariffMainItems` DROP FOREIGN KEY `FK_FMTariffMainItems_FMTariffMains_TariffId`;
-- Truncate data tariff DT
TRUNCATE TABLE `DTCostingMains`;
TRUNCATE TABLE `DTCostingCapacities`;
TRUNCATE TABLE `DTTariffMainItems`;
TRUNCATE TABLE `DTTariffMains`;
TRUNCATE TABLE `DTCostingVASs`;
TRUNCATE TABLE `DTTariffVASItems`;
TRUNCATE TABLE `DTTariffVASs`;
-- Truncate data tariff FM
TRUNCATE TABLE `FMCostingMains`;
TRUNCATE TABLE `FMCostingCapacities`;
TRUNCATE TABLE `FMTariffMainItems`;
TRUNCATE TABLE `FMTariffMains`;
-- Delete all record in tariff list
DELETE FROM `DTTariffMains` WHERE `Status`!='Temp';
-- Only delete record with Inactive status in tariff list
DELETE FROM `DTTariffMains` WHERE `Status` NOT IN ('Temp', 'Inactive');
-- Set valid from = current day
UPDATE `DTTariffMains` SET`ValidFrom`= CURDATE() WHERE `TariffCode`='VTC27062301072354DTSMC';
-- Set valid from = current day - 2
UPDATE `DTTariffMains` SET`ValidFrom`= CURDATE() - INTERVAL 2 DAY WHERE `TariffCode`='VTC06072311072394DTSMC';
-- Set all valid from = current day
UPDATE `DTTariffMains` SET`ValidFrom`= CURDATE();
-- Set valid to = current day
UPDATE `DTTariffMains` SET`ValidTo`= CURDATE();
-- Set valid to = current day - 1
UPDATE `DTTariffMains` SET`ValidTo`= CURDATE() - INTERVAL 1 DAY WHERE `TariffCode`='VTC06072311072394DTSMC';
-- Change create at & approval at
UPDATE `DTTariffMains` SET`CreateAt`='2023-07-01 08:03:22.213288', `ApprovalAt`='2023-07-01 08:08:26.981374' WHERE `TariffCode`='VTC04072309072329DTSMC';
-- Truncate data costing DT
TRUNCATE TABLE `DTBLCs`;
TRUNCATE TABLE `DTCapacities`;
TRUNCATE TABLE `DTCostings`;
TRUNCATE TABLE `DTVASs`;
-- Truncate data costing FM
TRUNCATE TABLE `FMBLCs`;
TRUNCATE TABLE `FMCapacities`;
TRUNCATE TABLE `FMCostings`;
TRUNCATE TABLE `FMSurcharges`;
TRUNCATE TABLE `FMVASs`;
-- Truncate data costing CC
TRUNCATE TABLE `CCCapacities`;
TRUNCATE TABLE `CCCostings`;
TRUNCATE TABLE `CCVASs`;
-- Truncate data costing WH
TRUNCATE TABLE `WHCapacities`;
TRUNCATE TABLE `WHCostings`;
TRUNCATE TABLE `WHVASs`;
-- Update unit name EN
UPDATE `BasicLocalCharges` SET`UnitNameEN`='awb' WHERE `ChargeNameVN`='Phí vận đơn đường Hàng Không';
-- Set volume range uom = sqm/month
UPDATE `DemandVolumeRanges` SET`VolumeRangeUOM`='sqm/month' WHERE `ChargeNameENs`='[Office leasing fee]';
DELETE FROM `VolumeRanges` WHERE `ProductCode`='FM' AND `ServiceCodes`='[FM-SEFCL]' AND `VolumeRangeUOM`='container' AND `VolumeRangeName`='15 - 30';
-- Set status, valid from, cost for DT Costing SOTRANS
UPDATE `DTCostings` SET`Status`='Confirmed' WHERE `SupplierId`='SUP0300645369';
UPDATE `DTCostings` SET`ValidFrom`= CURDATE() WHERE `SupplierId`='SUP0300645369';
UPDATE `DTCostings` SET`Cost`='5000000' WHERE `SupplierId`='SUP0300645369';
-- Set valid from = current day for DT VAS SOTRANS
UPDATE `DTVASs` SET`ValidFrom`= CURDATE() WHERE `SupplierId`='SUP0300645369';
-- Set status, valid from, cost for DT Costing GEMADEPT
UPDATE `DTCostings` SET`Status`='Confirmed' WHERE `SupplierId`='SUP0301116791';
UPDATE `DTCostings` SET`ValidFrom`= CURDATE() WHERE `SupplierId`='SUP0301116791';
UPDATE `DTCostings` SET`Cost`='20000000' WHERE `SupplierId`='SUP0301116791';
-- Set valid from = current day for DT Costing SOTRANS & GEMADEPT & TRANSIMEX & ITL & VINAFREIGHT
UPDATE `DTCostings` SET`ValidFrom`= CURDATE() 
WHERE (`SupplierId`='SUP0300645369' 
OR `SupplierId`='SUP0301116791'
OR `SupplierId`='SUP0301874259'
OR `SupplierId`='SUP0301909173'
OR `SupplierId`='SUP0302511219'
);
```

```sql
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (1, 'second', 'giây', 'sec', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.105826', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (2, 'minute', 'phút', 'min', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.127553', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (3, 'hour', 'giờ', 'hour', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.145081', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (4, 'day', 'ngày', 'day', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.162671', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (5, 'week', 'tuần', 'week', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.184753', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (6, 'month', 'tháng', 'month', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.202005', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (7, 'quarter', 'quý', 'quarter', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.220396', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (8, 'year', 'năm', 'year', 'time', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.236061', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (9, 'millimetre', 'mi-li-mét', 'mm', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.256051', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (10, 'centimetre', 'xen-ti-mét', 'cm', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.271374', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (11, 'metre', 'mét', 'm', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.286646', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (12, 'kilometre', 'ki-lô-mét', 'km', 'distance', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.303202', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (13, 'square metre', 'mét vuông', 'sqm', 'area', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.317453', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (14, 'cube metre', 'mét khối', 'cbm', 'volume, chargeable volume', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.329068', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (15, 'gram', 'gam', 'g', 'net weight, gross weight, chargeable weight', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.344705', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (16, 'kilogram', 'ki-lô-gam', 'kg', 'net weight, gross weight, chargeable weight', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.362840', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (17, 'ton', 'tấn', 'ton', 'net weight, gross weight, chargeable weight', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.375121', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (18, 'degree Celsius', 'độ C', '°C', 'temperature', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.386677', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (19, 'degree Fahrenheit', 'độ F', '°F', 'temperature', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.401969', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (20, 'shipment', 'lô hàng', 'shipment', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.414795', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (21, 'Drum', 'Thùng phuy', 'drum', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.429930', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (22, 'IBC Tank', 'Thùng nhựa IBC', 'IBC tank', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.446650', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (23, 'Pallet', 'Pallet', 'pallet', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.458636', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (24, 'Carton', 'Carton', 'carton', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.469795', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (25, 'Bag', 'Túi', 'bag', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.486237', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (26, 'Roll', 'Cuộn', 'roll', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.498066', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (27, 'Piece', 'Cái', 'piece', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.511384', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (28, 'Label', 'Nhãn', 'label', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.524914', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (29, 'Package', 'Kiện', 'package', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.535921', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (30, 'Customs Declaration Sheet', 'Tờ khai Hải quan', 'CDS', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.550633', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (31, 'Certificate', 'Chứng nhận ', 'Certificate', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.565683', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (32, 'Container', 'Container', 'container', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.576823', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (33, 'Inch', 'Inch', 'In', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.590443', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (34, 'Foot', 'Foot', 'ft', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.602677', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (35, 'Yard', 'Yard', 'yd', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.615305', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (36, 'Mile', 'Dặm', 'mi', 'length, width, height', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.627414', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (37, 'Pound', 'Pound', 'lb', 'net weight, gross weight, chargeable weight', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.643332', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (38, 'Ounce', 'Ounce', 'oz', 'net weight, gross weight, chargeable weight', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.655093', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (39, 'Revenue Ton', 'Revenue Ton', 'RT', 'net weight, gross weight, chargeable weight', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.667171', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (40, 'Job', 'Lần làm hàng', 'Job', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.681117', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (41, 'Case', 'Case', 'case', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.692433', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (42, 'House Bill of Lading', 'Vận đơn Nhà', 'HBL', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.703882', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (43, 'Master Bill of Lading', 'Vận đơn Chủ', 'MBL', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.718759', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (44, 'House Air Waybill', 'Vận đơn hàng không Nhà', 'HAWB', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.740130', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (45, 'Master Air Waybill', 'Vận đơn hàng không Chủ', 'MAWB', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.754136', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (46, 'set', 'bộ', 'set', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.768550', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (47, 'string', 'dây', 'string', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.788268', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (48, 'bar', 'thanh', 'bar', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.801524', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (49, 'Entry', 'Đăng ký', 'entry', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.812858', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (50, 'Truck', 'Xe tải', 'truck', 'package', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.825472', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (51, 'Time', 'Lần', 'time', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.844100', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (52, 'Project', 'Dự án', 'project', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.862544', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (53, 'Worker', 'Nhân công', 'worker', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.878637', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (54, 'Quota', 'Hạn ngạch', 'quota', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.901326', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (55, 'Permit', 'Giấy phép', 'permit', 'document', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.917784', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (56, 'Percentage', 'Phần trăm', 'percentage', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.936008', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (57, 'Person', 'Người', 'person', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.958312', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (58, 'Purchase Order', 'Đơn đặt hàng', 'PO', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:36.974888', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (59, 'Kit', 'Bộ dụng cụ', 'kit', 'shipment', '0001-01-01 00:00:00.000000', NULL, '2023-07-03 04:02:37.000186', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
INSERT INTO `Uoms` (`Id`, `UomNameEN`, `UomNameVN`, `Symbol`, `Quantity`, `DateCreated`, `CreatedBy`, `LastModifiedDate`, `LastModifiedBy`, `IsDeleted`, `DeletedBy`, `DateDeleted`, `IsActive`, `InUsedCount`) VALUES (60, 'Bundle', 'Bó', 'bundle', 'package', '2023-07-03 04:02:37.021178', 'sys', '2023-07-03 04:02:37.021178', 'sys', 0, NULL, '0001-01-01 00:00:00.000000', 1, '0');
```

```sql
DROP PROCEDURE IF EXISTS insertRowsToTariffList;
DELIMITER //

CREATE PROCEDURE insertRowsToTariffList()
BEGIN
DECLARE i INT DEFAULT 1; 
WHILE (i <= 60) DO
    INSERT INTO `DTTariffMains` (
    `Id`,
    `CreateAt`,
    `UpdateAt`,
    `IsPublish`,
    `IsDelete`,
    `CreateBy`,
    `TraceId`,
    `TariffCode`,
    `ApprovalBy`,
    `AggregateCount`,
    `DueDateWarningAts`,
    `CurrentInspector`,
    `ProcessFlows`,
    `LevelResetRejected`,
    `DeclineStep`,
    `Step`,
    `ValidFrom`,
    `ValidTo`,
    `Status`,
    `ApprovalAt`,
    `SubmitBy`,
    `SubmitAt`,
    `DeclineBy`,
    `DeclineAt`,
    `NextAutoSubmitNewAt`,
    `NextAutoApproveAt`) VALUES (
    '0',
    '2023-07-05 03:17:58.565736',
    '2023-07-05 06:09:58.834401',
    1,
    0,
    'Mr.Submitter',
    'a88aa23daf362b7c4a72d198daa54440',
    CONCAT('AUTO', CURDATE(), i),
    'Mr.Approval1 - Mr.Approval2 - Mr.Master',
    '{}',
    '[{"Date":"2023-07-08T00:00:00Z","Days":3},{"Date":"2023-07-09T00:00:00Z","Days":2},{"Date":"2023-07-10T00:00:00Z","Days":1}]',
    '{"User":{"Email":"master.man@email.com","Level":3,"Username":"Mr.MasterMan","IsApprover":true,"SelfStatus":null,"GeneralStatus":"Approved","ProcessActionAt":"2023-07-05T03:49:34.7754505Z","RoleDisplayName":"Leader Sale","NextActionDueDateAt":null},"Status":"Approved","RejectReason":null}',
    '[{"Email":"submitter@email.com","Level":0,"Username":"Mr.Submitter","IsApprover":false,"SelfStatus":null,"GeneralStatus":"Submitted","ProcessActionAt":"2023-07-05T03:17:58.566055Z","RoleDisplayName":"Junior Sale","NextActionDueDateAt":null},{"Email":"approval1@email.com","Level":1,"Username":"Mr.Approval1","IsApprover":true,"SelfStatus":null,"GeneralStatus":"Approved","ProcessActionAt":"2023-07-05T03:47:53.9262748Z","RoleDisplayName":"Middle Sale","NextActionDueDateAt":null},{"Email":"approval2@email.com","Level":2,"Username":"Mr.Approval2","IsApprover":true,"SelfStatus":null,"GeneralStatus":"Approved","ProcessActionAt":"2023-07-05T03:48:49.4226803Z","RoleDisplayName":"Senior Sale","NextActionDueDateAt":null},{"Email":"master.man@email.com","Level":3,"Username":"Mr.MasterMan","IsApprover":true,"SelfStatus":null,"GeneralStatus":"Approved","ProcessActionAt":"2023-07-05T03:49:34.7754505Z","RoleDisplayName":"Leader Sale","NextActionDueDateAt":null}]',
    NULL,
    0,
    4,
    '2023-07-03 00:00:00.000000',
    '2023-07-04 00:00:00.000000',
    'Active',
    '2023-07-05 03:49:34.775475',
    'Mr.Submitter',
    '2023-07-05 03:17:58.566153',
    NULL,
    NULL,
    NULL,
    NULL);
    SET i = i + 1;
END WHILE;
END;
//
CALL insertRowsToTariffList();
```
