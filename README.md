# 🏥 Crestview Medical Centre — Patient & Revenue Dashboard

> **A health tech data analytics case study** | Excel data cleaning · Business insights · Interactive web dashboard

![Dashboard Preview](preview.png)

---

## 📌 Project Overview

This project analyses patient and revenue data for **Crestview Medical Centre**, a private healthcare provider in London, UK. Starting from a messy, real-world-style dataset, the goal was to clean, transform, and visualise hospital performance data to support strategic decision-making.

Built as part of the **10Alytics Health Tech Case Study**, facilitated by Mark Olafare.

---

## 🎯 Business Problem

Crestview faced:
- **Duplicate records** across patient visits
- **Missing values** in critical fields (visit dates, discounts, service units)
- **Inconsistent formats** for diagnosis, department names, and costs
- **No visibility** into revenue performance, department efficiency, or patient value segments

---

## 🛠️ Tools & Skills Used

| Tool | Purpose |
|------|---------|
| Microsoft Excel | Data cleaning, transformation, calculated metrics |
| HTML / CSS / JavaScript | Interactive dashboard |
| Chart.js | Data visualisations |

---

## 📊 Dashboard Features

The interactive dashboard (`index.html`) includes:

- **5 KPI cards** — Total patients, net revenue, average revenue, pending payments, high-value patients
- **Revenue by Department** — Bar chart of net revenue per department
- **Payment Status** — Doughnut chart (Paid vs Pending)
- **Admission Type Split** — Outpatient / Inpatient / Emergency breakdown
- **Insurance vs Revenue** — Average net revenue per insurance type
- **Patient Value Segments** — High / Medium / Low distribution
- **Top Diagnoses** — Most common diagnoses by patient count
- **Monthly Visit Trend** — Line chart of visits over time
- **Auto-generated Insights** — Dynamic insight cards based on filtered data
- **Searchable & sortable patient table** with pagination
- **CSV upload** — Drop in your own dataset to replace sample data
- **Filters** — Department, admission type, insurance, payment status, value segment

---

## 📁 Project Structure

```
crestview-medical-dashboard/
│
├── index.html          # Interactive dashboard (open in any browser)
├── README.md           # This file
└── data/
    └── hospital_visits.csv   # Your cleaned dataset (export from Excel)
```

---

## 🚀 How to Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/crestview-medical-dashboard.git
   cd crestview-medical-dashboard
   ```

2. **Open the dashboard**
   ```bash
   # Simply open index.html in your browser
   open index.html       # macOS
   start index.html      # Windows
   xdg-open index.html   # Linux
   ```

3. **Load your dataset**
   - Export your cleaned Excel file as **CSV**
   - Click "Choose CSV File" in the dashboard
   - All charts and KPIs update automatically ✨

---

## 📐 Data Dictionary

| Column | Description | Type |
|--------|-------------|------|
| Visit ID | Unique identifier for each patient visit | Text |
| Patient ID | Unique identifier for each patient | Text |
| Patient Name | Full name of the patient | Text |
| Gender | Patient's gender | Text |
| Age | Patient age in years | Number |
| Visit Date | Date of the patient visit | Date |
| Admission Type | Outpatient / Inpatient / Emergency | Text |
| Department | Hospital department | Text |
| Doctor | Attending doctor | Text |
| Diagnosis | Primary condition diagnosed | Text |
| Procedure | Medical procedure performed | Text |
| Lab Test Cost | Cost of lab tests | Number |
| Consultation Fee | Doctor's consultation fee | Number |
| Medication Cost | Cost of medications | Number |
| Length of Stay (Days) | Duration of inpatient stay | Number |
| Insurance Type | Private / HMO | Text |
| Payment Status | Paid / Pending | Text |
| Total Charges | Lab + Consultation + Medication | Number |
| Discount (%) | Discount applied | Number |
| Net Revenue | Total Charges × (1 − Discount) | Number |
| Patient Value Segment | High (>£12k) / Medium (£7k–£12k) / Low (<£7k) | Text |
| Diagnosis Category | Grouped diagnosis category | Text |

---

## 🧹 Data Cleaning Steps (Excel)

1. **Removed duplicate** Visit ID and Patient ID entries
2. **Cleaned numeric columns** — removed spaces, converted text to numbers
3. **Standardised text fields** using TRIM and PROPER
4. **Fixed date formats** — unified all Visit Date entries
5. **Replaced missing discounts** with 0
6. **Filled missing Length of Stay** with 0 for outpatients
7. **Standardised inconsistent entries** in Diagnosis, Department, Admission Type

---

## 📈 Calculated Metrics

```
Total Charges  = Lab Test Cost + Consultation Fee + Medication Cost
Net Revenue    = Total Charges × (1 − Discount %)
Patient Value Segment:
  High   → Net Revenue > £12,000
  Medium → Net Revenue £7,000 – £12,000
  Low    → Net Revenue < £7,000
```

---

## 💡 Key Insights

- **Cardiology** and **Respiratory** departments are top revenue generators
- **Pending payments** represent a significant revenue leakage risk
- **High-value patients** are concentrated in Inpatient admissions
- **HMO-insured patients** tend to have higher average net revenue than Private
- **Malaria and Arthritis** are the most frequently diagnosed conditions

---

## 🔗 Connect

- LinkedIn: [Audrey Tetteh](https://linkedin.com/in/audreytetteh)
- Portfolio: [yourwebsite.com](https://yourwebsite.com)

---

*Built with ❤️ by **Audrey Tetteh** as part of the 10Alytics Health Tech Data Analytics Programme*

`#HealthTechAnalysis` `#DAAnalyticsWith10Alytics` `#DataCleaning` `#ExcelForAnalysis`
