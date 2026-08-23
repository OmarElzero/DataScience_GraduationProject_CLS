# Cardiovascular Disease Risk Prediction

A DEPI (Digital Egypt Pioneers Initiative) graduation project that builds an end-to-end machine learning pipeline to predict cardiovascular disease (CVD) risk from clinical, demographic, and lifestyle data. The project is organized into the standard data-science lifecycle — data exploration and preprocessing, exploratory data analysis and feature engineering, model development and optimization, and MLOps deployment — culminating in an XGBoost classifier served through an interactive Streamlit web application.

![Last Commit](https://img.shields.io/github/last-commit/OmarElzero/DataScience_GraduationProject_CLS)
![Top Language](https://img.shields.io/github/languages/top/OmarElzero/DataScience_GraduationProject_CLS)
![Repo Size](https://img.shields.io/github/repo-size/OmarElzero/DataScience_GraduationProject_CLS)

## Features

- Engineered clinical features: BMI categories (Underweight/Normal/Overweight/Obese), a composite `lifestyle_score` (smoking, alcohol, physical inactivity), and blood pressure categories (Normal, Elevated, Hypertension Stage 1/2)
- Trained **XGBoost** classifier on ~68,000 patient records using 15 key clinical biomarkers (age, cholesterol, blood pressure, BMI, etc.), reaching ~73.7% test accuracy and a 0.74 F1-score
- Saved, reusable inference artifacts: `preprocessor.pkl`, `feature_selector.pkl`, and `xgboost_best_model.pkl`
- A **Streamlit** web app (`Cardio_App.py`) that takes demographic, health, and lifestyle inputs, computes BMI/pulse pressure, and returns a real-time CVD risk prediction with a confidence score, plus interactive data-exploration visualizations
- Full project documentation: requirement gathering, stakeholder analysis, activity diagrams, context-level and level-1 data flow diagrams, KPIs, and a risk assessment

## Tech Stack

- **Python**, **Jupyter Notebook** for analysis and modeling
- **pandas**, **NumPy** for data manipulation
- **scikit-learn** for preprocessing pipelines (`ColumnTransformer`, encoders, scalers)
- **XGBoost** as the final classification model
- **Matplotlib**, **Seaborn** for visualization
- **Streamlit** for the deployed prediction web app
- **pickle** for model/preprocessor serialization

## Methodology

1. **Data Exploration & Preprocessing** (`Data Exploration,Collection and PreProcessing Reports/EDA_Report.ipynb`) — initial exploration of the raw cardiovascular dataset, cleaning, and outlier handling (height, weight, and blood pressure outliers replaced with medians)
2. **Data Analysis, Visualization & Feature Engineering** (`Data Analysis,Visualization and Feature Engineering Reports/Analysis.ipynb`) — univariate, bivariate, and multivariate analysis, plus derivation of BMI categories, `lifestyle_score`, and blood pressure categories
3. **Model Development & Optimization** (`Model Development and Optimzation Reports/Model.ipynb`) — training and tuning multiple classifiers, selecting XGBoost as the best performer, and exporting the fitted preprocessor, feature selector, and model as `.pkl` artifacts
4. **MLOps Deployment & Monitoring** (`MLOPS_Deployment_and_Monitoring_Reports/`) — packaging the trained pipeline for serving, with the finalized artifacts consumed directly by the Streamlit app
5. **Final Documentation** — consolidated project report and Milestone 1 planning documents (system analysis, requirements gathering, DFDs, KPIs, risk assessment)

## Project Structure

| Path | Description |
|---|---|
| `Cardio_App.py` | Streamlit web application that loads the trained pipeline and serves real-time predictions |
| `Data Exploration,Collection and PreProcessing Reports/` | Initial EDA notebook and reports |
| `Data Analysis,Visualization and Feature Engineering Reports/` | Deeper analysis and feature engineering notebook |
| `Model Development and Optimzation Reports/` | Model training notebook, `requirements.txt`, and exported model artifacts |
| `MLOPS_Deployment_and_Monitoring_Reports/` | Final deployment artifacts (`xgboost_best_model.pkl`, `preprocessor.pkl`, `feature_selector.pkl`) used by the app |
| `Milestone 1 Documents/` | Requirements, stakeholder analysis, DFDs, KPIs, and risk assessment documents |
| `Final Documentation/` | Consolidated final project report |

## Installation

```bash
git clone https://github.com/OmarElzero/DataScience_GraduationProject_CLS.git
cd DataScience_GraduationProject_CLS
pip install streamlit pandas numpy scikit-learn xgboost matplotlib seaborn
```

## Usage

Run the prediction web app (from the repository root, so it can find the model artifacts under `MLOPS_Deployment_and_Monitoring_Reports/`):

```bash
streamlit run Cardio_App.py
```

Then enter demographic (age, gender, height, weight), health (blood pressure, cholesterol, glucose), and lifestyle (smoking, alcohol, activity) values in the web form to get a risk prediction with a confidence score, along with interactive data visualizations.

## Demo

No live demo is available for this project.

---

**Author:** OmarElzero · [GitHub](https://github.com/OmarElzero)
Last updated: 2026-08-23
