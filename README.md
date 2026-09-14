# 🏨 Resort Hotel Booking Analysis & Cancellation Prediction

A comprehensive, competition-grade Data Analytics & Machine Learning project focused on analyzing hotel booking behaviors, identifying key drivers of cancellation, and building a highly accurate predictive model to optimize revenue and occupancy rates.

---

## 📌 Executive Dashboard Showcase

Here is a visual walk-through of the interactive Excel Dashboards developed for this project:

### 1. Executive Overview & Key Metrics
<img src="EXCEL/images/Screenshot 2026-09-14 072108.png" width="100%" alt="Executive Overview">

### 2. Cancellation Intelligence & Lead Time Dynamics
<img src="EXCEL/images/Screenshot 2026-09-14 072114.png" width="100%" alt="Cancellation Intelligence">

### 3. Revenue & ADR Analysis
<img src="EXCEL/images/Screenshot 2026-09-14 072124.png" width="100%" alt="Revenue Dynamics">

### 4. Market & Customer Segmentation
<img src="EXCEL/images/Screenshot 2026-09-14 072130.png" width="100%" alt="Market Segmentation">

### 5. Detailed KPI Analysis
<img src="EXCEL/images/Screenshot 2026-09-14 072136.png" width="100%" alt="KPI Deep Dive">

---

## 📊 Dataset Metrics Overview
- **Verified Dataset Scope:** 14,677 resort booking records across 35 attributes.
- **Overall Cancellation Rate:** **69.31%** (10,172 canceled bookings).
- **Average Daily Rate (ADR):** $101.18
- **Tools Used:** 
  - **Excel:** Dynamic Pivot Tables, Custom KPI Cards, Interactive Slicers, Multi-tab Dashboards.
  - **Python (VS Code / Jupyter):** Pandas, NumPy, Seaborn, SciPy (Chi-Square Testing), Scikit-Learn (Random Forest).
  - **Power BI & ML Deployment:** Model persisted via Joblib (`cancellation_rf_model.pkl`).
- **Final Model Accuracy:** **95.74%** (Verified after resolving Data Leakage).

---

## 🛠️ Key Analytical & ML Pipeline

### 1. Exploratory Data Analysis & Statistical Testing
- **Correlation Heatmap:** Mapped core drivers behind high cancellation risk.
- **Chi-Square Test of Independence:** Confirmed statistically significant dependency ($p < 0.05$) between `deposit_type` and cancellation status.
- **Lead Time Profiling:** Binned `lead_time` into distinct groups to pinpoint high-risk advance booking windows (>90 days).

### 2. Machine Learning Model Architecture
- **Data Leakage Mitigation:** Strictly removed target-revealing variables (`reservation_status`, `reservation_status_date`) to guarantee real-world evaluation integrity.
- **Preprocessing:** Applied One-Hot Encoding and feature scaling on train/test split.
- **Model Evaluation:** Trained a `RandomForestClassifier` yielding **95.74% Accuracy**.
- **Top Risk Factors Identified:** `lead_time`, `adr` (Average Daily Rate), `country`, and `deposit_type`.

---

## 💡 Strategic Business Recommendations
1. **Dynamic Deposit Policies:** Re-evaluate advance booking terms; enforce strict non-refundable rules for high `lead_time` reservations (>90 days).
2. **Channel Management:** Address high cancellation segments within specific OTA/Group distribution channels.
3. **Data-Driven Overbooking:** Leverage the ML model to safely re-list predicted cancellations in real time, increasing RevPAR and room utilization.
