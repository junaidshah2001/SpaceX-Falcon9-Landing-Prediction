# 🚀 SpaceX Falcon 9 Booster Reusability Prediction and Analysis

[![Python](https://img.shields.io/badge/python-3.8+-blue)](https://www.python.org/)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

---

## **Project Overview**

This project is an end-to-end data science analysis of historical SpaceX Falcon 9 rocket flights.  
The goal is to **predict the success of first-stage booster landings** using machine learning.  

It follows a complete data analysis pipeline, including:

- Data collection and cleaning  
- Exploratory data and geospatial analysis  
- Dashboarding for stakeholders  
- Model training and evaluation  

---

## **Key Objectives**

1. **Data Engineering**  
   - Aggregate and clean launch data from multiple sources (API, Wikipedia)  
   - Create a reliable binary target variable (`Class`) for landing success  

2. **Exploratory Data Analysis (EDA)**  
   - SQL and geospatial techniques to find trends, risk factors, and launch site insights  

3. **Business Intelligence (BI)**  
   - Interactive dashboard to visualize launch success rates  

4. **Machine Learning**  
   - Train multiple classification models to predict booster landing success  

---

## **Key Findings**

### **1. Model Performance**
| Model                    | Test Accuracy |
|---------------------------|---------------|
| Logistic Regression       | 83.33%        |
| Support Vector Machine    | 83.33%        |
| K-Nearest Neighbors       | 83.33%        |
| Decision Tree             | 77.78%        |

**Insights:**  
- Logistic Regression, SVM, and KNN perform best.  
- Decision Tree shows slightly lower performance due to potential overfitting.  

---

### **2. Geospatial Analysis**
- **Logistics:** Launch sites near highways (~0.72 km) and railways for transport  
- **Safety:** Sites near coastlines (~0.58 km) and away from cities (e.g., 23+ km from Titusville, FL)  

---

## **Project Workflow (Notebooks)**

### **Phase 1: Data Preparation**
1. `SpaceX_Falcon9_Data_Prep.ipynb`  
   - Combine API and historical data into a raw dataset  

2. `SpaceX_Falcon9_data_wrangling_feature_engineering.ipynb`  
   - Clean data, handle missing values, create target variable (`Class`) and `No. of Flights`  

---

### **Phase 2: Exploratory Data Analysis (EDA)**
3. `SpaceX_Falcon9_Launches_SQL_Analysis.ipynb`  
   - SQL queries to calculate KPIs like success rates by Orbit and LaunchSite  

4. `SpaceX_Falcon9_Geo_Analysis.ipynb`  
   - Geospatial analysis using Folium to map launch sites and analyze placement  

---

### **Phase 3: Deployment and Prediction**
5. `SpaceX_Falcon9_Dashboard.ipynb`  
   - Interactive dashboard with Dash and Plotly  

6. `SpaceX_Falcon9_Landing_Prediction.ipynb`  
   - Data preparation, hyperparameter tuning, and model evaluation  

---

## **Installation and Setup**

### **Prerequisites**
- Python 3.8+  
- Git  

### **Setup Instructions**
1. Clone the repository:
```bash
git clone https://github.com/YourUsername/SpaceX-Falcon9-Landing-Prediction.git
cd SpaceX-Falcon9-Landing-Prediction

