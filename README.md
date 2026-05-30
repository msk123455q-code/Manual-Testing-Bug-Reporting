# Assignment No. 3 – Bug Reporting & Release Notes

![QA Testing](https://img.shields.io/badge/Testing-Manual--QA-blue?style=for-the-badge)
![Documentation](https://img.shields.io/badge/Artifacts-Excel%20%2F%20Markdown-green?style=for-the-badge)

## 📌 Project Overview
This repository contains the deliverables for **Assignment No. 3 - Bug Reporting**. The objective of this project is to simulate an end-to-end manual testing verification cycle on an E-Commerce web platform, identifying critical functional and user interface (UI) defects, documenting them under industry-standard tracking schemas, and providing a final release readiness report.

### 📁 Deliverables Included
* **[Click Here to Download Full Excel Sheet](./BugReport_ShahidKhan_Assignment%20.xlsx)** * **Tab 1:** Bug Report Log
* **Tab 2:** Release Notes / Executive Summary

---

## 🐛 Bug Report Log

Below is the structured registry of defects uncovered during the manual exploratory testing cycle.

| Bug ID | Title / Summary | Environment | Severity | Steps to Reproduce | Expected Result | Actual Result |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **BUG-001** | Cart item count displays a negative number when removing items below zero | Windows 11, Google Chrome (Latest Version) | 🔴 Critical | 1. Navigate to the online product page.<br>2. Click "Add to Cart" on any product.<br>3. Go to the Shopping Cart page.<br>4. Rapidly click the "Remove / Minus (-)" icon multiple times. | The item count should stop at 0, and the item should be removed completely from the cart view. | The cart updates to display a quantity of "-3 Items", and the total price reflects a negative balance. |
| **BUG-002** | "Proceed to Checkout" button overlaps footer navigation links on smaller screens | Windows 11, Edge Browser (Window resized to 1024x768 resolution) | 🔵 Minor | 1. Add any item to the shopping cart.<br>2. Navigate to the Cart Summary page.<br>3. Resize the desktop browser window horizontally to a narrower width.<br>4. Scroll down to the bottom of the cart summary panel. | The "Proceed to Checkout" button should dynamically adjust its positioning or wrap cleanly within the viewport layout. | The button slides down and overlaps directly on top of the "Privacy Policy" link in the footer, obscuring text and making both unclickable. |
| **BUG-003** | Registration form accepts numbers and special characters in First Name field | macOS, Safari Browser | 🟡 Major | 1. Click on the "Sign Up / Register" icon in the header.<br>2. In the "First Name" input field, type `John123!@#`.<br>3. Fill out the remaining fields with valid test data.<br>4. Click the "Submit Registration" button. | An inline validation error should appear under the field stating: "First name can only contain alphabetical characters." | The form successfully submits, creates the profile, and prints "Welcome, John123!@#" on the dashboard header. |
| **BUG-004** | Broken placeholder image icon displayed for featured items section on home screen | Windows 11, Google Chrome (Latest Version) | 🔵 Minor | 1. Open the homepage of the web application.<br>2. Scroll down past the main banner to the "New Arrivals" carousel block.<br>3. Observe the product thumbnails. | Every product card should load a high-resolution marketing picture of the item. | The third product card ("Classic Leather Wallet") fails to fetch the media file and displays a broken image icon. |
| **BUG-005** | Promo code entry field crashes the page when entering strings longer than 50 characters | Windows 11, Firefox Browser | 🟡 Major | 1. Add an item to the cart and proceed to the checkout screen.<br>2. Locate the "Apply Promo Code" field box.<br>3. Copy and paste a random alphanumeric string of 100 characters into the box.<br>4. Click the "Apply" button. | The UI displays a warning message: "Invalid code sequence format or code too long." | The entire browser page turns blank, throws an uncaught JavaScript reference error in the console, and forces the user to reload the tab. |

---

## 📋 Release Notes - Alpha Testing Cycle v1.0.3

### 1. Summary of Activities
A comprehensive manual validation cycle was performed targeting the core end-to-end customer workflows of the web storefront platform. Testing efforts focused heavily on: Account Creation, Product Visualization, Cart Adjustment Engine, and Checkout Form Handling.

### 2. Metrics Breakdown
* **Total Quality Defects Identified:** 5
* **🔴 Critical Severity Bugs:** 1 *(System logic failure)*
* **🟡 Major Severity Bugs:** 2 *(Validation & Crash risks)*
* **🔵 Minor Severity Bugs:** 2 *(Visual alignment issues)*

### 3. Known Blockers & Regressions (Exclusions for Deployment)
* **`[BUG-001]`** The shopping cart allows mathematical underflow logic resulting in negative items and negative balances. This requires immediate re-architecture of the item counting script before moving to production.
* **`[BUG-005]`** Uncapped input parameters inside the coupon voucher input field allow character strings to throw a fatal application stack error, wiping out the active user state.

---

### 👨‍💻 Submitted By
* **Tester Name:** Shahid Khan  
* **Role:** QA Intern / Student Tester  
* **Project Assignment:** Assignment No. 3 - Bug Reporting Log
