# Cardiovascular Disease Risk Prediction

![Project Banner](https://via.placeholder.com/800x200.png?text=Cardiovascular+Disease+Risk+Prediction)  
*A machine learning model and web application to predict cardiovascular disease risk.*

---

## 📌 Table of Contents  
- [Project Overview](#-project-overview)  
- [Key Features](#-key-features)  
- [Installation](#-installation)  
- [Usage](#-usage)  
- [Data](#-data)  
- [Model Performance](#-model-performance)  
- [Deployment](#-deployment)  
- [Contributing](#-contributing)  
- [License](#-license)  

---

## 🎯 Project Overview  
**Objective**: Predict cardiovascular disease (CVD) risk using clinical, demographic, and lifestyle data.  
**Target Audience**: Clinicians, researchers, and individuals seeking proactive health insights.  

**Components**:  
1. **Data Analysis**: EDA, outlier handling, and feature engineering.  
2. **Predictive Model**: XGBoost classifier (73.67% test accuracy).  
3. **Web Application**: Streamlit app for real-time risk prediction and data exploration.  

---

## 🔑 Key Features  
- **Engineered Features**:  
  - BMI categories (`Underweight`, `Normal`, `Overweight`, `Obese`).  
  - `lifestyle_score` (smoking, alcohol, inactivity).  
  - Blood pressure categories (`Normal`, `Elevated`, `Hypertension Stage 1/2`).  
- **Model**: XGBoost with 15 key clinical biomarkers (e.g., age, cholesterol, blood pressure).  
- **App Functionality**:  
  - Real-time risk prediction with probability scores.  
  - Interactive visualizations (univariate, bivariate, multivariate analysis).  

---

## ⚙️ Installation  
1. Clone the repository:  
   ```bash  
   git clone https://github.com/yourusername/cvd-risk-prediction.git  
   cd cvd-risk-prediction  
Install dependencies:

bash
pip install -r requirements.txt  
Required Libraries:

Python 3.8+

pandas, NumPy, scikit-learn, XGBoost

Streamlit, Matplotlib, Seaborn

🚀 Usage
Run the Streamlit App:
bash
streamlit run app.py  
Input Fields:

Demographics: Age, gender, height, weight.

Health Metrics: Blood pressure, cholesterol, glucose.

Lifestyle: Smoking, alcohol, physical activity.

Output:

Risk Level: "High Risk" or "Low Risk" with a confidence score.

Dashboard: Explore data trends via interactive plots.

📊 Data
Dataset: cardio_data_processed.csv (68,205 records, 14+ features).
Key Variables:

Target: cardio (1 = CVD present, 0 = absent).

Features: age_years, ap_hi, ap_lo, bmi, cholesterol, lifestyle_score, etc.

Preprocessing:

Outliers in height, weight, and blood pressure were replaced with medians.

Categorical variables encoded for modeling.

📈 Model Performance
Best Model: XGBoost

Metric	Value
Test Accuracy	73.67%
F1-Score	0.74
Precision	0.74
Recall	0.74
Top Features:

Blood pressure (ap_hi, ap_lo).

Age (age_years).

BMI and obesity status.

🌐 Deployment
The application is deployed on Streamlit Cloud:
🔗 Live Demo

App Workflow:

User inputs health data.

Real-time calculation of BMI and pulse pressure.

Model predicts risk using preprocessed features.

