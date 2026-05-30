# ✈️ phpTravels Online Travel Booking System — Manual Testing & Bug Report

## 📌 Project Overview
This repository contains the comprehensive QA manual testing deliverables for **Assignment No. 3**. The focus of this project was an end-to-end exploratory and functional testing of the **phpTravels Online Travel Booking System** (`phptravels.net/demo`), identifying core functional flaws, visual regressions, UI/UX issues, and critical edge-case bypasses.

A total of **24 unique, high-impact bugs** were discovered, documented, and 100% verified via live page access across desktop and mobile-responsive layouts.

---

## 🧑‍💻 Tester & Session Information
* **Tester Name:** Shahid Khan
* **Course / Batch:** Cohort 9 : QA (Manual + Automation)
* **Project Name:** phpTravels Online Travel Booking System
* **Test Date:** May 30, 2026
* **Test Environment:** Chrome 124 / Windows 11 & Mobile Responsive (via Chrome DevTools)
* **Tools Used:** Manual Testing — Browser: Google Chrome, Mozilla Firefox, Mobile Responsive Viewports

---

## 📊 Executive Defect Metric Dashboard

| Severity | Defect Count | Representative Bug IDs & Descriptions |
| :---: | :---: | :--- |
| <kbd>🔴 **Critical**</kbd> | **2** | **BUG-003**: Currency mismatch at checkout<br>**BUG-022**: No booking reference on confirmation page |
| <kbd>🟠 **High**</kbd> | **9** | **BUG-001**: Past date booking allowance<br>**BUG-005**: "Book Now" functional on sold-out rooms<br>**BUG-006**: Social login integration 404 error<br>**BUG-012**: Unreplaced Lorem Ipsum placeholder content<br>**BUG-013**: Gallery component crash on viewport resize<br>**BUG-019**: Total checkout price calculation mismatch<br>**BUG-021**: Email confirmation requirement bypass |
| <kbd>🟡 **Medium**</kbd> | **9** | **BUG-004**: Result count mismatch in filter pane<br>**BUG-007**: Hotel star rating UI/data mismatch<br>**BUG-008**: Input validation failure on phone field<br>**BUG-011**: Search filters automatically resetting on pagination<br>**BUG-014**: `'undefined'` string displayed in room type label<br>**BUG-018**: Wishlist toggle state persistence failure<br>**BUG-020**: Broken review rating submission form<br>**BUG-024**: Leaflet/Google Map rendering error |
| <kbd>🟢 **Low**</kbd> | **4** | **BUG-010**: Duplicate autocomplete entry in location input<br>**BUG-015**: Raw HTML tags exposed in tooltip description<br>**BUG-016**: Duplicate newsletter subscription acceptance<br>**BUG-017**: Broken breadcrumb navigation link trail<br>**BUG-023**: Incorrect HTML page title on checkout page |
| **TOTAL** | **24** | **100% Verified via Live Environment Testing** |

---

## 🛠️ Defect Lifecycle Attributes Explained

The complete testing lifecycle was tracked using a detailed **Bug Report Ledger** (structured as shown in the repository files). Each defect includes:
1. **Bug ID:** Unique sequential identifier (`BUG-001` through `BUG-024`).
2. **Summary:** Concisely defines the defect nature, location, and condition.
3. **Component/Module:** Isolate the fault domain (e.g., `Hotels/Booking`, `Authentication`, `Cart/Checkout`).
4. **Steps to Reproduce (STR):** Clear, sequential atomic instructions to recreate the bug from a clean session state.
5. **Expected vs. Actual Result:** Highlight the exact variance between business logic requirements and current system behavior.
6. **Severity vs. Priority Matrix:** Classifies technical impact (Severity) against business urgency for fixing (Priority).

---

## 📁 Repository Structure
```bash
├── README.md               # Professional project presentation and overview
├── BUG_REPORT_LEDGER.jpg   # Complete high-resolution spreadsheet of the 24 logged defects
└── RELEASE_NOTES_SUMMARY.png# Executive dashboard summary including defect density metrics
