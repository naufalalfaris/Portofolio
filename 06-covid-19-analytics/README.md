# 🦠 COVID-19 Indonesia Analytics Dashboard

## Project Overview

The COVID-19 pandemic generated a massive amount of public health data across Indonesia, creating opportunities to analyze infection trends, regional disparities, and the impact of different pandemic waves. However, raw datasets often contain missing values, inconsistent formats, and fields that are not immediately suitable for analysis.

This project was developed as an end-to-end data analytics portfolio project to transform raw COVID-19 Indonesia data into actionable insights through data cleaning, exploratory analysis, cloud-based data warehousing, and interactive dashboard visualization. The objective was to build a complete analytics workflow that mirrors a real-world data analyst process—from raw data to business-ready insights.

---

## Business Problem

Government agencies, researchers, and decision-makers need reliable data to understand:

- How COVID-19 cases evolved over time
- Which provinces experienced the highest impact
- Whether population density influenced case distribution
- How severe different pandemic waves were
- Which regions had mortality rates significantly above the national average

The available dataset contained data quality issues that could affect the accuracy of analysis and reporting. Therefore, data preparation and validation became a critical first step before generating insights.

---

## Dataset

**Source:** COVID-19 Indonesia Public Dataset

### Dataset Size
- 31,822 rows
- 38 columns (raw dataset)
- Provincial-level daily COVID-19 statistics

### Key Variables
- Date
- Province
- Total Cases
- Active Cases
- Recovered Cases
- Death Cases
- Case Fatality Rate (CFR)
- Population Density
- Growth Factor

---

## Project Workflow

### 1. Data Cleaning & Preparation

The raw dataset was assessed for data quality issues before analysis.

Key cleaning activities included:

- Converting incorrect data types into appropriate formats
- Handling missing values using province-level median imputation
- Removing irrelevant columns
- Standardizing column structures
- Validating data consistency across records

After the cleaning process:

✅ 31,822 rows retained  
✅ 37 columns retained  
✅ 0 missing values

---

### 2. Exploratory Data Analysis (EDA)

To better understand the pandemic's behavior across Indonesia, exploratory analysis was conducted using Python.

Seven analytical visualizations were created to investigate:

- Daily COVID-19 trends
- Monthly case distribution
- Provincial case comparisons
- Case Fatality Rate (CFR) by province
- Growth Factor trends
- Correlation between variables
- Relationship between population density and COVID-19 cases

The analysis helped identify anomalies, trends, and regional differences that were later incorporated into the dashboard.

---

### 3. Data Pipeline Development

To simulate a modern analytics workflow, an end-to-end pipeline was designed:

```text
Excel
   ↓
Python (Pandas)
   ↓
CSV
   ↓
Google Sheets
   ↓
BigQuery
   ↓
Looker Studio
```

This structure allows data to move from raw processing into cloud-based storage and visualization while maintaining reproducibility.

---

### 4. SQL Data Transformation

Before visualization, the cleaned data was transformed inside BigQuery to create analysis-ready datasets.

Seven BigQuery Views were developed using:

- Common Table Expressions (CTE)
- Window Functions
- CASE WHEN logic
- Aggregations and ranking functions

These views served as the primary data source for dashboard reporting.

---

### 5. Dashboard Development

An interactive dashboard was built in Looker Studio to provide a comprehensive view of COVID-19 conditions in Indonesia.

### Dashboard Structure

#### Page 1 — National Overview
- Total cases
- Active cases
- Recoveries
- Deaths
- National trends over time

#### Page 2 — Pandemic Wave Analysis
- Growth Factor analysis
- Rolling Average trends
- Delta vs Omicron comparison

#### Page 3 — Geographic Analysis
- Provincial performance comparison
- Regional case distribution
- CFR by province

#### Page 4 — Deep-Dive Insights
- Population density analysis
- Correlation analysis
- High-risk province identification

### Dashboard Metrics

- 4 dashboard pages
- 24 visualizations
- Interactive filters and controls

---

## Key Findings

### 1. Significant CFR Disparities Across Provinces

The national Case Fatality Rate (CFR) averaged approximately **2.47%**, but several provinces recorded substantially higher mortality rates.

Notable examples:

- Lampung: ~5–6%
- East Java: ~5–6%

This indicates considerable regional differences in healthcare outcomes and pandemic impact.

---

### 2. Delta Wave Was More Severe Than Omicron

Analysis of Growth Factor and Rolling Average metrics showed that:

- The Delta wave (July 2021) produced a sharper increase in cases
- Peak case growth was significantly higher during Delta
- Omicron generated large case volumes but lower relative severity

This finding aligns with broader observations regarding the impact of the Delta variant.

---

### 3. Most Cases Occurred During the Recovery Phase

An unexpected finding was that the majority of recorded cases occurred during the "Mereda" (Recovery) phase rather than the "Kritis" (Critical) phase.

This occurred because:

- Recovery periods lasted significantly longer
- Cases accumulated over extended durations
- Critical periods were shorter but more intense

This insight highlights the importance of considering duration when interpreting pandemic phases.

---

## Tools & Technologies

### Data Processing
- Python
- Pandas

### Data Storage & Transformation
- Google BigQuery
- SQL

### Data Visualization
- Looker Studio

### Supporting Tools
- Microsoft Excel
- Google Sheets

---

## Skills Demonstrated

- Data Cleaning
- Data Validation
- Exploratory Data Analysis (EDA)
- SQL Query Development
- BigQuery Data Warehousing
- Data Pipeline Design
- Dashboard Development
- Data Storytelling
- Insight Generation
- Business Intelligence

---

## Project Outcome

This project demonstrates the complete data analytics lifecycle, from raw data preparation to executive-level reporting. By combining Python, SQL, BigQuery, and Looker Studio, the project delivers a scalable analytics solution capable of transforming complex public health data into clear, actionable insights.
