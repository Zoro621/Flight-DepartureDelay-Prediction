Flight Departure Delay Prediction
📌 Overview

This project focuses on predicting flight departure delays using historical flight and weather data.
The dataset was provided in raw .docx files, which were first converted into structured CSV format for preprocessing and modeling.

The project consists of:

Data preprocessing & feature engineering

Exploratory Data Analysis (EDA)

Regression and Classification models

Prediction on test dataset

Kaggle submission file generation

🎯 Objectives

Extract and preprocess flight + weather data.

Engineer features such as delay duration, time-based attributes, and weather factors.

Perform EDA to analyze patterns in delays.

Build predictive models for:

Binary Classification (On-time vs Delayed).

Multi-Class Classification (No Delay, Short, Moderate, Long).

Regression (Exact delay duration).

Generate predictions on the test dataset in Kaggle submission format.

⚙️ Workflow
1. Data Preprocessing

Extracted structured flight data from .docx files.

Cleaned missing values.

Converted all time fields into datetime format.

Merged with weather data.

Engineered features:

Departure Delay (minutes).

Day of Week, Hour of Day, Month.

Weather factors (temperature, wind speed, visibility).

2. Exploratory Data Analysis

Delay Distributions: Histograms of departure delays.

Temporal Patterns: Line/bar plots for delays across days, hours, months.

Airline & Airport Analysis: Delay patterns grouped by airlines and airports.

Weather Correlation: Relationship between delays and weather conditions.

3. Modeling

Binary Classification → Logistic Regression, Random Forest, etc.

Multi-Class Classification → Decision Trees, Random Forest, etc.

Regression → Linear Regression, Random Forest Regressor.

Evaluation Metrics:

Classification → Accuracy, Precision, Recall, F1-score, Confusion Matrix.

Regression → MAE, RMSE.

4. Model Optimization

Applied Grid Search/Random Search for hyperparameter tuning.

Used Cross-validation to ensure reliable results.

Compared models and selected best-performing ones.

5. Testing & Submission

Applied trained models to test dataset.

Generated Kaggle-ready CSV files with predictions:

Regression → r_predictions.csv

Binary Classification → b_predictions.csv

Multi-Class Classification → m_predictions.csv

📊 Results

Binary Classification: [0.73, 0.42]

Multi-Class Classification: [0.99, 0.99]

Regression: [25.6, 8.5]

🚀 Tools & Libraries

Python

Pandas, NumPy – Data cleaning & preprocessing

Matplotlib, Seaborn – Visualization

Scikit-learn – Machine Learning models

📁 Project Files

ml_proj.ipynb → Main notebook with all preprocessing, EDA, modeling, and predictions.

predictions.csv → Final predictions in Kaggle submission format.

TRAIN

TEST

WEATHER

README.md → Project description.

✅ Assumptions

Flights without actual departure times were dropped.

Weather features represent departure airport conditions at scheduled time.

Outliers in delay duration were handled (capping/removal).