# Aadhaar_Service_Delivery_Analysis
#### Exploratory Data Analysis (EDA) using Python & Interactive Dashboards in Power BI

## Table of Contents
- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Dataset Details](#dataset-details)
- [Tools & Technologies](#tools--technologies)
- [Methodology](#methodology)
- [Project Structure](#project-structure)
- [Python EDA Visualization](#python-eda-visualization)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [ Conclusion](#conclusion)
- [How to Run This Project](#how-to-run-this-project)
- [Author & Contact](#author--contact)


---

## Overview
Aadhaar Service Delivery Analytics project analyzes Aadhaar enrolment, demographic updates, and biometric activity to understand coverage and service delivery patterns across India. Using aggregated UIDAI datasets, the analysis examines regional, age-wise, and temporal variations across States, Districts, and Pincodes. The project focuses on New Aadhaar Enrolment, Demographic Enrolment and Update Metrics, and Biometric Enrolment and Authentication Metrics. Key trends and patterns are visualized to support administrative monitoring and reporting. The insights aim to enable data-driven governance and informed policy planning.
## Problem Statement
Aadhaar is India’s foundational digital identity system, enabling access to welfare schemes, public services, and financial inclusion at a national scale. Given its extensive reach, systematic analysis of Aadhaar enrolment and update data is essential to understand population coverage, regional participation, and evolving demographic and biometric patterns over time.

This project leverages large-scale administrative data to analyse Aadhaar enrolment and update activities with the objective of uncovering meaningful societal and operational insights. Using three UIDAI datasets—New Aadhaar Enrolment , Demographic Enrolment  (Name, Date of Birth, Gender, Address), and Biometric Enrolment and Authentication (Fingerprint, Iris, and Facial Capture)—the analysis examines regional, demographic, and temporal variations across states, districts, and pincodes.

The study focuses on identifying disparities in age-group coverage, trends in New Aadhaar Enrolments, patterns in biometric enrolment indicators (fingerprint, iris, and facial capture), and the frequency and distribution of demographic updates such as address changes. By detecting spatial anomalies, coverage imbalances, and under-served populations, the project aims to highlight service delivery gaps and operational inefficiencies.

The overarching objective is to transform complex Aadhaar datasets into actionable, evidence-based insights that can support informed policy formulation, targeted governance interventions, and system optimisation, thereby contributing to a more inclusive, efficient, and responsive digital identity ecosystem in India.


## Dataset Details
Source of data: event.data.gov.in

 Raw Dataset Size: overall 4.84 Million records
1. New Adhar Enrolment Dataset (1006029 (1.0 M) rows, 7 columns)
2. Demographic Update Dataset (2071700 (2.071 M) rows, 6 columns)
3. Biometric Enrolment Dataset (1766212 (1.76 M) rows, 6 columns)

Cleaned Dataset Size: Overall 4.34 Million records
1. New Adhar Enrolment Dataset (983072 (0.98 M) rows, 14 columns)
2. Demographic Update Dataset (1598097 (1.59 M) rows, 13 columns)
3. Biometric Enrolment Dataset (1861108 (1.86 M) rows, 13 columns)

Key fields/variables: date, state, district, pincode, month_ name, Children(0-17) Age, Adult(18+) Age

## Tools & Technologies

Python 🐍 (Pandas, NumPy, Seaborn, Matplotlib) – used for Exploratory Data Analysis, Correlation Analysis  and Statistical Analysis.

Power BI 📊 – used for KPI cards, Charts, Slicers, Dashboard interactive Creation.


## Methodology
1. Data Ingestion and Understanding: Imported and consolidated multiple Aadhaar CSV files using Pandas to create unified enrolment, demographic, and biometric datasets for analysis.

2. Data Cleaning and Preprocessing: Standardized State, District, and Pincode fields, handled missing and invalid values, derived temporal attributes (Month), and created analytical features using Pandas and NumPy to support structured analysis.

3. Data Exploration: This stage focuses on understanding the dataset’s structure, scope, and quality by examining variables, data types, record volumes, missing values, and overall data distribution using Python (Pandas, NumPy).

4. Exploratory Data Analysis (EDA): This phase involves statistical analysis and correlation analysis, along with univariate, bivariate, and trivariate visualizations, to identify patterns, trends, relationships, and anomalies across enrolment, demographic, biometric, and geographic dimensions using Python (Matplotlib, Seaborn).

5. Data Visualization: Interactive dashboards were designed and developed using Power BI to present key insights through KPI cards, trend analyses, geographic breakdowns, enabling clear interpretation and decision-support for governance and service delivery optimization.




## Project Structure


```bash
uidai-data-hackathon-adhaar-service-delivery-analytics/
│
├── README.md
├── .gitignore
│
├── dashboard/
│   └── Aadhaar_Service_Delivery_Analytics.pbix
│
├── datasets/
│   ├── cleaned_new_aadhaar_enrolment_data.csv
│   ├── cleaned_demographic_update_data.csv
│   └── cleaned_biometric_enrolment_data.csv
│
├── python_scripts/
│   ├── new_aadhaar_enrolment.ipynb
│   ├── demographic_update_enrolment.ipynb
│   └── biometric_update_enrolment.ipynb
│
├── report/
│   └── Aadhaar_Service_Delivery_Analysis_Report.pdf
│
├── snapshots/
│   ├── New Aadhaar Enrol.png
│   ├── Demographic Update Enrol.png
│   ├── Biometric Update Enrol.png
│   ├── State-wise New Aadhaar Enrol.png
│   ├── State-wise Demographic Enrol.png
│   ├── State-wise Biometric Enrol.png
│   ├── District-wise New Aadhaar Enrol.png
│   ├── District-wise Demographic Enrol.png
│   ├── District-wise Biometric Enrol.png
│   ├── Pincode-wise New Aadhaar Enrol.png
│   ├── Pincode-wise Demographic Enrol.png
│   ├── Pincode-wise Biometric Enrol.png
│   └── Bottom 30 Pincode-wise Enrol.png
```

## Dashboard
POWERBI Dashboard Shows:

1. New Aadhaar Enrolment Analytics Dashboard:
Visualizes new Aadhaar enrolments across states, districts, and PIN codes with age-wise distribution and monthly trends, enabling analysis of child-driven enrolment patterns, geographic concentration, and academic or outreach-linked demand.

2. Aadhaar Demographic Enrolment Dashboard:
Analyzes demographic update volumes by geography, age group, and time, highlighting adult-dominated update behavior, urban concentration, service coverage across districts and PIN codes, and compliance-driven temporal peaks.

3. Aadhaar Biometric Enrolment Dashboard:
Tracks biometric update activity across regions, age groups, and months, revealing sustained high-volume system usage driven by lifecycle updates, identity verification needs, and uneven geographic distribution.


![New Aadhaar Enrol](snapshots/New%20Aadhaar%20Enrol.png)
![Demographic Update Enrol](snapshots/Demographic%20Update%20Enrol.png)
![Biometric Update Enrol](snapshots/Biometric%20Update%20Enrol.png)

## Python EDA Visualization
![State-wise New Aadhaar Enrol](snapshots/State-wise%20New%20Aadhaar%20Enrol.png)
![State-wise Demograpgic Enrol](snapshots/State-wise%20Demograpgic%20Enrol.png)
![State-wise Biometric Enrol](snapshots/State-wise%20Biometric%20Enrol.png)
![District-wise New Aadhaar Enrol](snapshots/District-wise%20New%20Aadhaar%20Enrol.png)
![District-wise Demograpgic Enrol](snapshots/District-wise%20Demograpgic%20Enrol.png)
![District-wise Biometric Enrol](snapshots/District-wise%20Biometric%20Enrol.png)
![Pincode-wise New Aadhar Enrol](snapshots/Pincode-wise%20New%20Aadhar%20Enrol.png)
![Pincode-wise Demographic Enrol](snapshots/Pincode-wise%20Demographic%20Enrol.png)
![Pincode-wise Biometric Enrol](snapshots/Pincode-wise%20Biometric%20Enrol.png)
![Bottom 30 Pincode-wise Enrol](snapshots/Bottom%2030%20Pincode-wise%20Enrol.png)
![Monthly Trend](snapshots/Monthly%20Trend.png)


## Key Insights
1.	System-wide scale and maturity: Aadhaar service delivery has transitioned to an update-led usage model, recording 5.33M new enrolments, 36.6M demographic updates, and over 68M biometric transactions, reflecting sustained nationwide utilization rather than enrolment expansion.
2.	Clear age-wise functional separation: New Aadhaar enrolments are predominantly driven by children (0–17 years), while adults (18+) account for the majority of demographic and biometric updates, underscoring Aadhaar’s role in service access, compliance, and identity verification.
3.	State-level concentration in high-population regions: High volumes of enrolment and update activity are concentrated in large, high-population states, where population scale and administrative density naturally generate higher Aadhaar service demand.
4.	District and PIN code-level urban skew: Urban and semi-urban districts and PIN code areas record disproportionately higher enrolment and update volumes due to migration inflows, dense settlements, and better-developed Aadhaar infrastructure.
5.	Persistent underperformance in low-population and remote areas: Lower enrolment and update volumes are concentrated in rural, low-population, and geographically challenging regions, where dispersed settlements, limited infrastructure, and accessibility constraints suppress service throughput.
6.	Predictable temporal demand patterns across services: New Aadhaar enrolments peak in July and September in line with academic cycles, demographic updates surge in March, November, and December due to compliance and welfare deadlines, while biometric enrolments remain consistently high year-round (6–9M per month).


## Recommendations 
1.	Expand last-mile access in low-coverage areas: Scale up mobile enrolment units, temporary camps, and decentralized centres in rural, remote, hilly, and tribal districts and low-performing PIN code areas to address physical access and geographic constraints.
2.	Strengthen Aadhaar infrastructure and operator capacity: Increase the availability of permanent centres, biometric devices, and trained operators, supported by regular training, system uptime monitoring, and adequate staffing to improve service reliability and throughput.
3.	Adopt population-adjusted, demand-based planning metrics: Move beyond absolute volumes by using per-capita and population-normalized KPIs at state, district, and PIN code levels to enable equitable planning and fair performance evaluation.
4.	Implement age-responsive and institution-linked service models: Institutionalize school-, Anganwadi-, and hospital-based enrolment for children (0–17), and bank, workplace, and welfare-office-linked update services for adults (18+) to reduce service friction and improve coverage.
5.	Align operational capacity with predictable demand cycles: Proactively scale staffing, appointment slots, and system capacity during academic admissions, financial year-end compliance periods, and welfare scheme rollouts to manage peak demand efficiently.
6.	Strengthen outreach, decentralization, and monitoring mechanisms: Enhance local awareness campaigns, expand service delivery through CSCs, post offices, panchayats, and urban local bodies, and use real-time district- and PIN-code-level dashboards to enable timely corrective action.

## Conclusion
Aadhaar service delivery has matured into an update-driven system, with demand concentrated in urban high-population areas and among adults, underscoring the need for targeted, data-driven interventions to ensure equitable nationwide access.


 
## How to Run This Project

1. Clone the Repository:
```bash
git clone https://github.com/Anjaneyak24/uidai-data-hackathon-adhaar-service-delivery-analytics.git
```
2. Click the links below to open the Python scripts:
- [new_aadhaar_enrolment.ipynb](python_scripts/new_aadhaar_enrolment.ipynb)
- [demographic_update_enrolment.ipynb](python_scripts/demographic_update_enrolment.ipynb)
- [biometric_update_enrolment.ipynb](python_scripts/biometric_update_enrolment.ipynb)


3. Click the link below to view the Power BI Dashboard
 - [Aadhaar_Service_Delivery_Analytics.pbix](dashboard/Aadhaar_Service_Delivery_Analytics.pbix)

 4. Click the link below to view the Report:
 - [Aadhaar_Service_Delivery_Analysis_Report.pdf](report/Aadhaar_Service_Delivery_Analysis_Report.pdf)  

5. Click the links below to view the Datasets

Note: Full Aadhaar datasets exceed GitHub’s file size limits. Hence, sample datasets (~1.5 lakh records each) have been uploaded to enable reproducibility and analysis.

 - [cleaned_new_aadhaar_enrolment_data](datasets/cleaned_new_aadhaar_enrolment_data.csv)
 - [cleaned_demographic_update_data](datasets/cleaned_demographic_update_data.csv)
 - [cleaned_biometric_enrolment_data](datasets/cleaned_biometric_enrolment_data.csv)

## Author & Contact

**Anjaneya K**  
_Data Analyst_  
📧 Email: anjaneya.data@gmail.com

Phone No. : 8123499976