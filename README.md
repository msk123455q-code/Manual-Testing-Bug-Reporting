# Manual-Testing-Bug-Reporting
Assignment No. 3 - Manual Bug Reporting and Release Notes for an E-Commerce Platform.
# Assignment No. 3 – Bug Reporting & Release Notes

## 📌 Project Overview
This repository contains a comprehensive manual validation cycle performed targeting the core end-to-end customer workflows of an E-Commerce web platform. Testing efforts focused on: Account Creation, Product Visualization, Cart Adjustment Engine, and Checkout Form Handling.

### 🛠️ Included Artifacts
* **[Click Here to Download the Full Excel Bug Log](./Assignment3_Bug_Reporting_YourName.xlsx)** (Make sure this filename matches your exact uploaded file name!)

---

## 📊 Executive Testing Summary
* **Total Quality Defects Identified:** 5
* **🔴 Critical Severity Bugs:** 1 (System logic failure)
* **🟡 Major Severity Bugs:** 2 (Validation & Crash risks)
* **🔵 Minor Severity Bugs:** 2 (Visual alignment issues)

---

## 🐛 Highlights of Identified Bugs

### BUG-001: Cart item count displays a negative number when removing items below zero
* **Severity:** Critical
* **Steps to Reproduce:**
  1. Navigate to the online product page and click "Add to Cart".
  2. Go to the Shopping Cart page.
  3. Rapidly click the "Remove / Minus (-)" icon multiple times.
* **Expected Result:** The item count should stop at 0, and the item should be removed completely from the cart view.
* **Actual Result:** The cart updates to display a quantity of "-3 Items", and the total price reflects a negative balance.

### BUG-003: Registration form accepts numbers and special characters in First Name field
* **Severity:** Major
* **Steps to Reproduce:**
  1. Click on the "Sign Up / Register" icon in the header.
  2. In the "First Name" input field, type `John123!@#`.
  3. Click the "Submit Registration" button.
* **Expected Result:** An inline validation error should appear under the field stating: "First name can only contain alphabetical characters."
* **Actual Result:** The form successfully submits, creates the profile, and prints "Welcome, John123!@#" on the dashboard header.

---

## 📋 Release Notes - Alpha Testing Cycle v1.0.3
### Known Blockers & Regressions (Exclusions for Production Deployment)
* **[BUG-001]** The shopping cart allows mathematical underflow logic resulting in negative items and negative balances. This requires immediate re-architecture of the item counting script before moving to production.
* **[BUG-005]** Uncapped input parameters inside the coupon voucher input field allow character strings to throw a fatal application stack error, wiping out the active user state.
