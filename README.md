# 📊 HR Leave Management System (Excel)

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

https://forms.gle/azLXLp68RVP1zqGv6

### 2. Leave Log (Main Database)
- Stores all validated leave records
- Contains calculated fields such as number of leave days
- Acts as the central data source

<img width="1012" height="537" alt="Leave Log" src="https://github.com/user-attachments/assets/93a8a636-e4ed-488f-81c1-3785316d84b7" />

### 3. Summary Dashboard Sheet
- Aggregates leave usage per employee
- Calculates remaining leave balances
- Provides HR overview and insights

<img width="1366" height="617" alt="Summary" src="https://github.com/user-attachments/assets/f0894c9c-2734-404b-a200-cf615169526e" />

---

## 📌 Key Formulas Used

The system relies on Excel/Google Sheets formulas such as:

### Total Leave Calculation
```excel
=SUMIFS(LeaveLog!F:F,LeaveLog!B:B,A2,LeaveLog!C:C,"Sick Leave",LeaveLog!G:G,"Approved")

```

 ### Number of Leave Days
 ```excel
=DATEDIF(StartDate,EndDate,"d")+1
```

### Employee Lookup
 ```excel
=VLOOKUP(A2,Employees!A:B,2,FALSE)
```

### Dynamic Employee List
 ```excel
=UNIQUE(LeaveLog!B:B)
```

## 📌 Dashboard & Visual Design

The Summary Sheet functions as a lightweight HR dashboard featuring:

- Leave usage per employee  
- Remaining leave balances  
- Conditional formatting:  
  - 🔴 Red → No leave remaining  
  - 🟡 Yellow → Low balance  
  - 🟢 Green → Healthy balance  
- Automated updates based on new entries  

---

## 📌 Key Insights

- Leave usage varies significantly across employees  
- Sick leave is typically taken in smaller, frequent intervals  
- Annual leave is usually taken in bulk periods  
- The system helps identify employees nearing leave exhaustion  
- Automation reduces manual HR workload  

---

## 📌 Tools Used

- Microsoft Excel / Google Sheets  
- Data Validation (Dropdown lists)  
- Conditional Formatting  
- SUMIFS, DATEDIF, VLOOKUP, IF functions  
- Google Forms (optional input method)  

---

## 📌 Project Deliverables

- Automated Leave Management System  
- Structured Leave Log database  
- Dynamic Summary Dashboard  
- Conditional formatting alerts system  
- Scalable HR tracking framework  

---

## 📌 Limitations

- No payroll integration  
- Manual approval process required  
- No automated notifications (email/SMS)  
- Designed for small to medium teams  

---

## 📌 Potential Extensions

This project can be extended into:

- Power BI HR Analytics Dashboard  
- Automated approval workflows (Google Apps Script)  
- Email notification system for leave requests  
- Payroll system integration   



