## NYC Airbnb Price 

## Prediction 🏡 

Predicting Airbnb listing prices in New York City using Linear Regression, with a focus on thorough data cleaning, outlier treatment, and feature engineering. 

## 📌 Project Overview 

This project builds a regression model to predict Airbnb listing prices in NYC based on features like room type, location, and availability. The goal was to practice a complete end-to-end ML workflow — from raw, messy real-world data to a trained and evaluated model. 

## Dataset 📊 

Source: NYC Airbnb Open Data (Kaggle) Size: 48,895 listings, 16 columns 

## Target variable: `price` 

## Workflow 🔧 

## 1. Data Cleaning 

- Dropped irrelevant columns: `id` , `name` , `host_id` , `host_name` , `last_review` 

- Filled missing `reviews_per_month` values with 0 

- Checked and confirmed no duplicate rows 

## 2. Exploratory Data Analysis (EDA) 

- Visualized distributions of `price` and `minimum_nights` using boxplots and 

- histograms 

- Identified heavy right-skew and extreme outliers in both features 

## 3. Outlier Treatment 

- Capped `price` at the 99th percentile (₹799) 

- Capped `minimum_nights` at the 95th percentile (30 nights) 

Removed listings with `price` ≤ 0 

Rows reduced from 48,895 → 43,961 

## 4. Feature Engineering 

One-hot encoded 

- `neighbourhood_group` and `room_type` 

Dropped high-cardinality 

- `neighbourhood` column 

## 5. Modeling 

Train-test split: 80/20 

Model: `LinearRegression` (scikit-learn) 

## 📈 Results 

|Metric|Value|
|---|---|
|R² Score|0.365|
|MAE|51.49|
|MSE|6734.59|
|RMSE|82.06|



## 🔍 Key Insight 

The R² of 0.365 shows a linear model captures only part of the price variation — Airbnb pricing depends on non-linear factors (location desirability, amenities, seasonality) that a straight-line model can't fully represent. Next step: experimenting with tree-based models like Random Forest or XGBoost to capture these non-linear patterns. 

## 🛠 Tools & Libraries 

Python 

- Pandas, NumPy 

- Matplotlib, Seaborn 

- Scikit-learn 

## 📂 Files 

- `minor_project_2.ipynb` — full notebook 

- with EDA, preprocessing, and model training 

## 🚀 Future Improvements 

- Try Random Forest / XGBoost for non-linear relationships 

- Frequency or target encoding for the 

- `neighbourhood` feature instead of 

- dropping it 

- Hyperparameter tuning and crossvalidation 

- Feature importance analysis 

