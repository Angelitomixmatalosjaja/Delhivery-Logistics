# Delhivery-Logistics
# 🚚 Delhivery Logistics Delivery Time Analysis

This project analyzes delivery data from **Delhivery**, one of India’s largest logistics companies, to uncover insights into delivery duration, optimize scheduling, and build predictive models.

---

## 📦 Dataset Overview

- **Records:** ~144,000 deliveries  
- **Key fields:**
  - `od_start_time`, `od_end_time` (timestamps)
  - `actual_time`, `osrm_time` (real vs estimated)
  - `route_type`, `cutoff_factor`, `segment_*`
  - `source_name`, `destination_name`, coordinates

---

## 🎯 Objectives

- Clean and enrich delivery data  
- Analyze time patterns and operational bottlenecks  
- Train machine learning models to predict delivery duration  
- Provide actionable business recommendations  

---

## 🔧 Data Preparation

- Converted timestamps to datetime format  
- Created new features:
  - `hour`, `day_of_week`, `is_weekend`
  - `estimation_error`, `efficiency_ratio`, `is_late`
- Filled missing names based on geocoordinates  

---

## 📊 Key Insights

- Deliveries between **7 AM and 9 PM** experience a drop of over **6,000 orders**, making it an optimal dispatch window.  
- Average delivery time in that window drops from **~70 to ~20 minutes**.  
- `route_type` and `cutoff_factor` significantly impact delivery efficiency.  

---

## 🤖 Models Used

- **Regression:** Linear & Random Forest to predict delivery duration  
- **Classification:** Random Forest Classifier to predict late deliveries  
- **Clustering:** KMeans to segment delivery patterns  

---

## 📈 Evaluation

- **Mean Absolute Error (MAE):** 14 minutes  
- **R² Score:** 0.05 (baseline model — low due to limited features)  

---

## 📌 Recommendations

- Schedule more deliveries between **7 AM – 9 PM**  
- Include **weather, traffic, and categorical location data**  
- Consider using **XGBoost** and **GridSearch** for hyperparameter tuning  

---

## 📁 Project Structure
|- data/
|- notebooks/
|- images/
|- README.md
|- delhivery_analysis.py


---

## 🚀 Next Steps

- Add time-based and categorical features  
- Automate alerts on delivery time deviations  
- Build **Streamlit** dashboards or **Power BI** reports for stakeholders  
