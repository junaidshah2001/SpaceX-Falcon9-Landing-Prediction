🚀 SpaceX Falcon 9 Booster Reusability Prediction and Comprehensive Analysis
Project Overview
This is an end-to-end data science project focused on the historical flight data of the SpaceX Falcon 9 rocket. The primary goal is to develop a robust machine learning model capable of predicting the success of the first-stage booster landing (reusability).

The project follows a complete, structured data analysis pipeline, covering everything from raw data collection and cleaning to advanced geospatial analysis, dynamic dashboarding, and final model training.

🎯 Key Objectives
Data Engineering: Aggregate and clean launch data from multiple sources (API, Web Scraping) and engineer a reliable binary target variable (Class).

Exploratory Analysis (EDA): Utilize SQL and geospatial techniques to uncover key trends, risk factors, and strategic launch site placements.

Business Intelligence (BI): Create an interactive dashboard for stakeholders to visually assess performance and confirm analytical hypotheses.

Machine Learning: Train and evaluate multiple supervised classification models to find the most accurate predictor of landing success.

📊 Key Findings and Results
1. Model Performance (Prediction)
Four machine learning models were trained and tuned on the final feature-engineered dataset:

Logistic Regression: Achieved a test accuracy of 83.33%. This model performs well, indicating a linear relationship between some features and the landing outcome.

Support Vector Machine (SVM): Also achieved a test accuracy of 83.33%, demonstrating strong separation capability.

K-Nearest Neighbors (KNN): Matched the top accuracy score of 83.33%, suggesting that success/failure cases cluster well in the feature space.

Decision Tree: Achieved a lower test accuracy of 77.78%, making it less reliable than the other three models.

2. Strategic Insights (Geospatial Analysis)
The analysis of launch site locations using Folium confirmed a strategic balance between logistics and safety:

Logistics: Launch sites show close proximity to highways (around 0.72 km) and railways to facilitate transportation of components.

Safety: Sites are intentionally located near the coastline (around 0.58 km) to allow launches over the ocean and maintain a safe distance from major cities (e.g., over 23 km from Titusville, FL for CCAFS LC-40).

🛠️ Project Workflow (Notebooks)
The entire project is documented step-by-step across the following six Jupyter Notebooks, located in the notebooks/ directory.

Phase 1: Data Preparation
SpaceX_Falcon9_Data_Prep.ipynb: Focuses on combining data from the SpaceX API and historical records (Wikipedia) into a unified raw dataset.

SpaceX_Falcon9_data_wrangling_feature_engineering.ipynb: Cleans the data, handles missing values (using mean imputation for PayloadMass), and creates the binary target variable (Class) and the No. of Flights feature.

Phase 2: Exploratory Data Analysis (EDA)
SpaceX_Falcon9_Launches_SQL_Analysis.ipynb: Performs strategic EDA using SQL queries on a temporary database to calculate KPIs like success rates by Orbit and LaunchSite.

SpaceX_Falcon9_Geo_Analysis.ipynb: Uses Folium and geospatial distance calculations to map launch sites and analyze their strategic placement relative to key infrastructure and populated areas.

Phase 3: Deployment and Prediction
SpaceX_Falcon9_Dashboard.ipynb: Implements a dynamic BI dashboard using Dash and Plotly to enable visual exploration of success rates filtered by Launch Site and Payload Mass range.

SpaceX_Falcon9_Landing_Prediction.ipynb: The final step: prepares data (standardization, split), tunes hyperparameters, and evaluates the performance of the four supervised classification models.

⚙️ Installation and Setup
Prerequisites
Python 3.8+

Git

Setup Instructions
Clone the Repository:

git clone [https://github.com/YourUsername/SpaceX-Falcon9-Landing-Prediction.git](https://github.com/YourUsername/SpaceX-Falcon9-Landing-Prediction.git)
cd SpaceX-Falcon9-Landing-Prediction

Create Virtual Environment:

python -m venv venv
source venv/bin/activate  # Use `venv\Scripts\activate` on Windows

Install Dependencies:

pip install -r requirements.txt

Running the Analysis
After setup, launch Jupyter and execute the notebooks in numerical order (1 through 6) to reproduce the entire project pipeline:

jupyter notebook
