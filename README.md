# 🧪 Manual QA Testing Practice: Web Authentication Module (Jira)

## 📌 Project Overview
This repository documents my hands-on **Manual Quality Assurance (QA)** practice focused on functional and negative testing for a web-based **User Authentication (Login) Module**. 

The primary objective of this project is to validate input handling, boundary conditions, and error messaging to ensure system security and prevent unauthorized access—critical standards in financial and digital banking applications. All test cases, execution statuses, and defect tracking workflows were managed using **Jira**.

---

## 🛠️ Tools & Test Environment
* **Test Management & Bug Tracking:** Jira Software (Kanban Board)
* **Testing Methodology:** Black-Box Testing, Negative Testing, Boundary Value Analysis (BVA)
* **Browser:** Google Chrome
* **Operating System:** Windows 11

---

## 📋 Test Case Summary

| Test Case ID | Test Scenario | Testing Type | Priority | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **TC-001** | Login with an invalid password | Negative | Highest | System denies access and displays *"Invalid password"* notification. | User bypasses authentication and directly enters the next page. | ❌ **Fail** *(Bug)* |
| **TC-002** | Login with a password shorter than 8 characters | Boundary / Negative | Highest | System validates length, denies access, and displays minimum character warning. | System denies access and displays the expected validation message. | ✅ **Pass** |
| **TC-003** | Login with an unregistered email address | Negative | Medium | System denies access and displays *"Account is not registered"* notification. | System denies access and displays the expected notification. | ✅ **Pass** |
| **TC-004** | Login with empty email and password fields | Negative | Medium | System denies access and displays *"Email and Password are required"* warning. | System denies access and displays the expected warning. | ✅ **Pass** |

---

## 🔍 Detailed Test Cases & Defect Findings

### ❌ TC-001: Login with an Invalid Password *(Critical Security Defect)*
* **Pre-condition:** User has a registered email account.
* **Test Steps:**
  1. Navigate to the login page.
  2. Enter a registered email address.
  3. Enter an incorrect password.
  4. Click the **Login** button.
* **Expected Result:** Authentication fails; user remains on the login page with an error prompt (`"Invalid password"`).
* **Actual Result:** Authentication is bypassed; user is redirected directly to the authenticated dashboard/next page.
* **Severity / Priority:** Critical / Highest (Security Vulnerability).

### ✅ TC-002: Login with Password Shorter Than 8 Characters
* **Test Steps:**
  1. Navigate to the login page.
  2. Enter a registered email address.
  3. Enter a password containing fewer than 8 characters (e.g., `1234567`).
  4. Click the **Login** button.
* **Expected Result:** System enforces minimum length validation and blocks login attempt.
* **Actual Result:** Matches expected result.

### ✅ TC-003: Login with Unregistered Email
* **Test Steps:**
  1. Navigate to the login page.
  2. Enter an unregistered email address.
  3. Enter any random password.
  4. Click the **Login** button.
* **Expected Result:** System blocks login and alerts that the account is not registered.
* **Actual Result:** Matches expected result.

### ✅ TC-004: Login with Blank Mandatory Fields
* **Test Steps:**
  1. Navigate to the login page.
  2. Leave both **Email** and **Password** fields empty.
  3. Click the **Login** button.
* **Expected Result:** System blocks submission and prompts user to fill in required fields.
* **Actual Result:** Matches expected result.

---

## 📸 Jira Board & Execution Evidence

* **Jira Kanban Board Overview:** `jira-board-overview.png`
* **TC-001 Defect Documentation:** `tc-001-detail.png`

---

## 👤 Author
**Muhammad Rizki Adzani**  
* **LinkedIn:** [://linkedin.com](www.linkedin.com/in/muhammad-rizki-adzani)  
* **GitHub:** [://github.com](https://github.com/muhammadrizkiadzani-dot)  
* **Email:** muhammadrizkiadzani@gmail.com
