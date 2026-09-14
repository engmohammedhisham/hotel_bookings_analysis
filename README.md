# 🏨 Resort Hotel Booking Analysis & Cancellation Prediction

A comprehensive, competition-grade Data Analytics & Machine Learning project focused on analyzing hotel booking behaviors, identifying key drivers of cancellation, and building a highly accurate predictive model to optimize revenue and occupancy rates.

---

## 📌 Project Overview
- **Dataset:** 14,684 booking records with 32 attributes.
- **Overall Cancellation Rate:** ~37.04%
- **Tools Used:** 
  - **Excel:** Advanced Pivot Tables, Dynamic Charts, Multi-tab Dashboards (Executive, Market, Revenue, Cancellation Intelligence).
  - **Python (VS Code / Jupyter):** Pandas, NumPy, Seaborn, Matplotlib, SciPy (Chi-Square), Scikit-Learn (Random Forest).
- **Final Model Accuracy:** **95.74%** (Verified after Data Leakage removal).

---

## 🛠️ Key Phases & Workflow

### 1. Exploratory Data Analysis & Statistical Testing
- **Correlation Heatmap:** Identified numerical features strongly associated with cancellations.
- **Chi-Square Test of Independence:** Statistically confirmed ($p < 0.05$) the dependency between `deposit_type` and booking cancellation.
- **Density Distribution:** Visualized how higher `lead_time` exponentially increases cancellation probability.

### 2. Machine Learning Model Development
- Resolved **Data Leakage** by removing direct outcome predictors (`reservation_status`, `reservation_status_date`).
- Applied **One-Hot Encoding** for categorical variables and split dataset (80% Train / 20% Test).
- Trained a **RandomForestClassifier** achieving a robust **95.74% Accuracy**.
- **Top Predictors Identified:** `lead_time`, `adr` (Average Daily Rate), `country`, and `deposit_type`.

---

## 💡 Executive Business Recommendations
1. **Stricter Lead Time Policies:** Enforce non-refundable deposits for bookings made >90 days in advance.
2. **Channel Rate Management:** Re-evaluate terms with Online Travel Agencies (OTAs) and Group segments exhibiting high cancellation rates.
3. **Data-Driven Overbooking:** Leverage the ML model to safely re-list rooms predicted to be canceled, maximizing RevPAR and room utilization.

---

## 🚀 How to Run the Project
1. Clone the repository:
   ```bash
   git clone [https://github.com/engmohammedhisham/hotel-booking-analysis.git](https://github.com/engmohammedhisham/hotel-booking-analysis.git)