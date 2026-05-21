# 🏥 Massachusetts General Hospital — Patient Records Analysis

> A complete Python/Jupyter Notebook data analysis project covering
> patient encounters, cost & coverage insights, and patient behavior
> at Massachusetts General Hospital from 2011 to 2022.

---

## 👨‍💻 Author

| | |
|---|---|
| **Analyst** | Dr. Bahaa |
| **Organization** | Bahaa Pharmacy — Data Analytics Division |
| **Location** | Dirout, Assiut, Egypt |
| **Date** | May 2026 |

---

## 📋 Project Overview

This project analyzes synthetic patient records from Massachusetts
General Hospital spanning 11 years (2011–2022). The dataset was
generated using the **Synthea Synthetic Patient Generator** and
covers ~974 patients, 27,891 hospital encounters, and 47,701
medical procedures.

The analysis is structured around three core objectives:

| # | Objective | Key Questions |
|---|---|---|
| 1 | **Encounters Overview** | Volume trends, class breakdown, length of stay |
| 2 | **Cost & Coverage Insights** | Claim costs, payer coverage, expensive procedures |
| 3 | **Patient Behavior** | Admissions over time, 30-day readmissions, top patients |

---

## 📁 Repository Structure

```
hospital-patient-records/
│
├── hospital_analysis.ipynb       ← Main Jupyter Notebook
│
├── data/
│   ├── patients.csv              ← Patient demographics (974 rows)
│   ├── encounters.csv            ← Hospital visits (27,891 rows)
│   ├── procedures.csv            ← Medical procedures (47,701 rows)
│   ├── payers.csv                ← Insurance companies (10 rows)
│   ├── organizations.csv         ← Hospital info (1 row)
│   └── data_dictionary.csv       ← Column definitions
│
├── outputs/
│   ├── objective1_encounters_overview.png
│   ├── objective2_cost_coverage.png
│   ├── objective3_patient_behavior.png
│   └── final_dashboard.png
│
├── sql/
│   ├── create_hospital_db.sql
│   └── hospital_analytics_questions.sql
│
├── citation.txt                  ← Dataset source citation
└── README.md                     ← This file
```

---

## 📊 Dataset Summary

| File | Description | Rows | Columns |
|---|---|---|---|
| `patients.csv` | Demographics, DOB, marital status | 974 | 20 |
| `encounters.csv` | Visit dates, class, cost, payer | 27,891 | 14 |
| `procedures.csv` | Procedure codes, descriptions, cost | 47,701 | 9 |
| `payers.csv` | Insurance company details | 10 | 7 |
| `organizations.csv` | Hospital name and location | 1 | 8 |

> **Data Source:**
> Jason Walonoski et al., *Synthea: An approach, method, and software
> mechanism for generating synthetic patients*, Journal of the American
> Medical Informatics Association, Volume 25, Issue 3, March 2018.
> https://doi.org/10.1093/jamia/ocx079

---

## 🔧 Requirements

### Python Version
```
Python 3.8+
```

### Libraries
```
pandas >= 3.0.2
numpy >= 2.4.4
matplotlib >= 3.10.8
seaborn >= 0.13.2
jupyter
```

### Installation
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

---

## 🚀 How to Run

1. Clone or download this repository
2. Place all CSV files inside the `data/` folder
3. Open a terminal and navigate to the project folder
4. Launch Jupyter Notebook:
```bash
jupyter notebook hospital_analysis.ipynb
```
5. Run all cells in order:
```
Kernel → Restart & Run All
```

---

## 🗂️ Notebook Structure

| Step | Title | Description |
|---|---|---|
| 1 | Setup & Library Imports | Import libraries, set chart styles and color palette |
| 2 | Data Loading & First Look | Load all 5 CSV files, inspect shape and dtypes |
| 3 | Data Cleaning & Type Casting | Fix dtypes, extract features, calculate LOS and AGE |
| 4 | KPI Summary | Calculate and print 8 high-level KPIs |
| 5 | Objective 1 — Encounters Overview | 3 analyses + 3 charts |
| 6 | Objective 2 — Cost & Coverage | 4 analyses + 4 charts |
| 7 | Objective 3 — Patient Behavior | 3 analyses + 3 charts |
| 8 | Final Dashboard | 6 KPI cards + 6 charts in one professional view |
| 9 | Conclusions & Recommendations | Key findings and 3 actionable recommendations |

---

## 📌 Key KPIs

| KPI | Value |
|---|---|
| Total Unique Patients | 974 |
| Total Encounters | 27,891 |
| Avg. Encounters per Patient | 28.6 |
| Avg. Length of Stay | 1.5 days |
| Avg. Total Claim Cost | $3,639.68 |
| Insurance Coverage Rate | 51.3% |
| Avg. Out-of-Pocket Cost | $2,524.72 |
| 30-Day Readmission Rate | 60.2% |
| Total Procedures Performed | 47,701 |

---

## 🔍 Key Findings

### Objective 1 — Encounters Overview
- Activity peaked in **2014 (3,885 encounters)** and dipped in 2019–2020 (COVID impact)
- **Ambulatory visits** dominate every year at 50%+ of all encounters
- **99.7%** of all encounters were under 24 hours — the hospital is primarily outpatient

### Objective 2 — Cost & Coverage
- **48.7% of encounters (13,586)** had zero insurance coverage ⚠️
- Most expensive procedure: **Admit to ICU at $206,260** average
- Most frequent procedure: **Health & social care assessment (4,596 times)**
- **Medicaid** generated the highest average claim cost at **$6,205**

### Objective 3 — Patient Behavior
- **60.2% of encounters** were 30-day readmissions ⚠️
- Top readmitted patient had **1,375 readmissions** — strong chronic disease signal
- Clear **COVID-19 dip** visible in 2019–2020 quarterly admissions

---

## 🎯 Recommendations

1. **Address the Insurance Coverage Gap**
   Nearly half of all encounters have zero payer coverage. The hospital
   should explore financial assistance programs, Medicaid enrollment
   support, and patient payment plans.

2. **Chronic Care Management Program**
   The top 15 readmitted patients account for a disproportionate share
   of all 30-day readmissions. A dedicated management program targeting
   high-frequency patients could significantly reduce unnecessary visits.

3. **Monitor Post-COVID Recovery**
   The 2021 rebound is promising but 2022 data is incomplete (only 220
   encounters). A full 2022–2023 analysis is recommended to confirm
   the recovery trend is sustained.

---

## 📸 Dashboard Preview

![Final Dashboard](outputs/final_dashboard.png)

---

*Built with ❤️ using Python & Jupyter Notebook*
*Dr. Bahaa — Bahaa Pharmacy, Data Analytics Division — May 2026*
