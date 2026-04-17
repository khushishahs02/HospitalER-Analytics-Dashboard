# 🏥 Hospital Emergency Room Dashboard — Project Documentation

**Author:** Khushi  
**Tool:** Microsoft Power BI  
**Date:** April 2026  
**Status:** In Progress

---

## Project Overview

This project is a **Hospital Emergency Room (ER) Analysis Dashboard** that I am building using **Microsoft Power BI**. The goal is to transform raw ER operational data into a powerful, interactive visual analytics solution that helps hospital administrators, department heads, and healthcare decision-makers **track, analyze, and optimize** emergency room performance.

Emergency rooms are the frontline of any hospital, they operate under immense pressure with unpredictable patient volumes, critical wait times, and the constant need to balance quality of care with operational efficiency. This dashboard is designed to bring **clarity to that chaos** by surfacing key performance indicators (KPIs) and trends that drive smarter, data-driven decisions.

---

## Problem Statement

Hospital emergency departments face several recurring operational challenges:

- **Unpredictable patient volumes** make staffing and resource allocation inefficient.
- **Long and inconsistent wait times** directly impact patient outcomes and satisfaction.
- **Low visibility into satisfaction trends** means quality-of-care issues go unnoticed until they escalate.
- **Unbalanced departmental referrals** lead to bottlenecks in specific departments while others remain underutilized.
- **Lack of demographic and temporal analysis** prevents targeted interventions for specific patient groups or time periods.

Without a centralized analytics solution, hospital management relies on fragmented reports and gut instinct leading to reactive rather than proactive decision-making.

**This dashboard solves that.**

---

## Objective

To design and develop an interactive, multi-page Power BI dashboard that enables stakeholders to:

1. **Monitor real-time ER performance** through key metrics and KPIs.
2. **Identify patterns and anomalies** in patient flow, wait times, and satisfaction.
3. **Drill down into demographics** (age, gender, race) to uncover disparities or targeted needs.
4. **Analyze departmental referral loads** to optimize inter-department resource allocation.
5. **Make data-driven decisions** that improve patient care, reduce wait times, and enhance overall operational efficiency.

---

## Key Performance Indicators (KPIs)

The dashboard tracks and visualizes the following core KPIs:

### 1. Number of Patients
- Measures the **total number of patients** visiting the ER on a daily basis.
- Displayed as a daily trend using an **area sparkline** to reveal patterns over time — such as peak days, seasonal surges, or unusual dips.
- **Insight:** Helps administration anticipate high-traffic periods and plan staffing accordingly.

### 2. Average Wait Time
- Calculates the **average time a patient waits** before being attended to by a medical professional.
- Visualized through a **daily area sparkline** to highlight days with abnormally high wait times.
- **Insight:** Directly correlates with patient satisfaction and clinical outcomes; enables identification of operational bottlenecks.

### 3. Patient Satisfaction Score
- Tracks the **average satisfaction score** of patients on a daily basis to evaluate quality of service.
- Presented as a **daily trend line** to identify dips in satisfaction and correlate them with peak times or operational disruptions.
- **Insight:** Acts as a quality-of-care barometer; helps pinpoint when and why patient experience deteriorates.

### 4. Number of Patients Referred
- Counts the **number of patients referred** from the ER to specific departments each day.
- Tracked using an **area sparkline** to spot daily trends and departments with consistently high referral rates.
- **Insight:** Identifies departments under disproportionate load, enabling targeted resource reallocation and capacity planning.

---

## 📑 Dashboard Structure (4 Pages)

I am building this dashboard across **4 distinct pages**, each designed to answer specific analytical questions:

| Page | Title | Focus Area |
|------|-------|------------|
| 1 | **Monthly Overview** | High-level KPIs, patient volume trends, and monthly snapshot of ER performance |
| 2 | **Patient Demographics** | Breakdown by age group, gender, and race — identifying who visits the ER and when |
| 3 | **Time & Referral Analysis** | Heatmaps and trends for wait times by hour/day, plus departmental referral patterns |
| 4 | **Satisfaction & Performance** | Deep dive into satisfaction trends, correlation with wait times, and performance benchmarks |

> *Detailed visuals and preview screenshots for each page will be added as the dashboards are completed.*

---

## 🔍 Insights & Business Problems Solved

### ✅ Staffing Optimization
By analyzing patient volume trends across days and hours, the dashboard reveals **when the ER is busiest** — enabling management to schedule adequate staff during peak periods and reduce overstaffing during lulls.

### ✅ Wait Time Reduction
Tracking average wait times daily exposes **systemic delays**. If wait times spike consistently on certain days or during certain hours, it signals a need for process improvement, additional triage staff, or resource reallocation.

### ✅ Patient Experience Improvement
The satisfaction score trend line acts as an **early warning system**. A sudden dip in scores, when correlated with wait time spikes or high patient volumes, reveals the root cause — enabling targeted interventions before patient complaints escalate.

### ✅ Departmental Load Balancing
Referral data highlights which departments receive the most ER patients. If one department (e.g., Orthopedics or Cardiology) is consistently overloaded while others are underutilized, the hospital can **redistribute resources** or adjust referral protocols.

### ✅ Demographic-Driven Decisions
Understanding the **age, gender, and racial composition** of ER visitors helps hospitals tailor their services — whether it's adding pediatric resources, addressing health disparities, or designing community outreach programs for underserved groups.

### ✅ Proactive vs. Reactive Management
Instead of reacting to crises after they happen, the dashboard puts **trends and patterns front and center** — empowering leadership to anticipate problems and act before they impact patients.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Microsoft Power BI** | Dashboard design, data modeling, DAX calculations, and interactive visualizations |
| **DAX (Data Analysis Expressions)** | Custom measures and calculated columns for KPIs |
| **Power Query (M Language)** | Data cleaning, transformation, and loading (ETL) |
| **Excel / CSV** | Source data format |

---

## 📂 Project Structure

```
hospital-er-dashboard/
├── Assets/                  # Images, icons, and schema diagrams
├── Dashboard/               # Power BI report files (.pbix)
├── Data/                    # Source data
│   ├── Raw/                 # Original, untouched data files
│   └── Cleaned/             # Processed data (currently moved to Raw for modeling)
├── Documentation/           # Project logs and references
│   ├── Project_Documentation.md
│   ├── PROJECT_TIMELINE.md  # Detailed project progress summary
│   └── Terminology.pdf
├── Scripts/                 # Code and calculation scripts
│   ├── DAX/                 # Power BI measures and table expressions
│   └── PowerQuery/          # M scripts for data transformation
├── .gitignore
├── README.md
└── LICENSE, etc.
```

---

## 🚀 What's Next

- [x] Complete data cleaning and transformation in Power Query
- [x] Build DAX measures for all 4 KPIs
- [/] Design and develop all 4 dashboard pages (Page 1 complete)
- [x] Add interactivity (slicers, drill-throughs, cross-filtering)
- [ ] Capture dashboard previews and add them to the documentation
- [ ] Final review and publish

---

## 📬 Contact

**Khushi**  
*Data Analytics Enthusiast*  
📧 Feel free to reach out for collaboration or feedback!

---

> *This documentation is a living document and will be updated as the project progresses.*
