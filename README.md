# 📊 HR Leave Management System (Excel / Google Sheets Project)

---

## 📌 Table of Contents

- [Project Overview](#project-overview)
- [Business Problem](#business-problem)
- [Data Sources](#data-sources)
- [Data Cleaning & Preparation](#data-cleaning--preparation)
- [System Structure (Data Model)](#system-structure-data-model)
- [Key Formulas Used](#key-formulas-used)
- [Dashboard & Visual Design](#dashboard--visual-design)
- [Key Insights](#key-insights)
- [Tools Used](#tools-used)
- [Project Deliverables](#project-deliverables)
- [Limitations](#limitations)
- [Potential Extensions](#potential-extensions)
- [Note](#note)
- [Author](#author)

---

## 📌 Project Overview

This project is a simulated HR Leave Management System built using Excel. It automates the tracking of employee leave balances across multiple categories such as Annual Leave, Sick Leave, Paternity Leave, Maternity Leave, and Compassionate Leave.

The system demonstrates how HR teams can manage leave requests, track usage, and monitor remaining balances using structured data, formulas, and automated calculations.

---

## 📌 Business Problem

Organizations often face challenges such as:

- Manual tracking of employee leave in spreadsheets
- Errors in calculating remaining leave balances
- Lack of visibility into leave usage trends
- Inefficient approval and record-keeping processes

This project solves these issues by building a structured and automated leave tracking system that improves accuracy, transparency, and efficiency.

---

## 📌 Data Sources

This is a simulated project. All data was created to replicate a real-world HR environment.

### Data Inputs:
- Employee master list (simulated)
- Leave request records (simulated)
- Leave policy rules:
  - Annual Leave (10 days)
  - Sick Leave (5 days)
  - Paternity Leave (14 days)
  - Maternity Leave (90 days)
  - Compassionate Leave (configurable)

---

## 📌 Data Cleaning & Preparation

The dataset was cleaned and structured to ensure consistency:

- Standardized date formats
- Removed duplicate entries
- Ensured consistent leave type naming
- Validated employee IDs using dropdown lists
- Restricted status values to: Approved, Pending, Rejected

---

## 📌 System Structure (Data Model)

The project is built using three core components:

### 1. Leave Request Input Sheet
- Captures raw leave requests via form

### 2. Leave Log (Main Database)
- Stores all validated leave records
- Contains calculated fields such as number of leave days
- Acts as the central data source

### 3. Summary Dashboard Sheet
- Aggregates leave usage per employee
- Calculates remaining leave balances
- Provides HR overview and insights

---

## 📌 Key Formulas Used

The system relies on Excel/Google Sheets formulas such as:

### Total Leave Calculation
```excel
=SUMIFS(LeaveLog!F:F,LeaveLog!B:B,A2,LeaveLog!C:C,"Sick Leave",LeaveLog!G:G,"Approved")
