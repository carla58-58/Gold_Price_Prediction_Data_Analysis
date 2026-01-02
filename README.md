# Gold_Price_Prediction_Data_Analysis

**View the interactive notebook on Google Colab:**  
[Open in Google Colab](https://colab.research.google.com/drive/1yEbTnvRKcr6HgyBFbgLOESkB-SYXM_EM?authuser=1#scrollTo=2At6vbGgB6i_)

## 1. Project Overview

**Objective:**  
Predict gold ETF (GLD) prices using Random Forest regression on historical financial data.

**Key Questions:**

- How well can ML predict gold prices from market indicators?
- Which features (SPX, SLV, Oil, EUR/USD) correlate most with gold?
- What's the model's prediction accuracy (R² score)?

**Dataset:**  

- **Source:** `gld_price_data.csv`
- **Features:** Date, GLD (target), SPX, GLD, USO, SLV, EUR/USD

## 2. Data Loading & Initial Inspection

- Loaded data from `gld_price_data` (2292 rows, 7 columns)
- Checked head/tail, shape, info(), describe(), nulls (no missing values)
- Examined data types and statistical summary

## 3. Data Cleaning

  - No major cleaning needed (no nulls/duplicates found)
  - Selected numeric columns for analysis (dropped Date)
  - Verified data quality ready for modeling

## 4. Exploratory Data Analysis (EDA)

- **Correlation Analysis:**
  - Heatmap of numeric features (cbar=True, annot=True)
  - GLD correlations printed (strongest with SLV, SPX)
 
- **Price Distribution:**
  - Histogram of GLD prices (green, KDE overlay)

## 5. Feature Preparation & Splitting

- **Features/Target:**
  - X: SPX, GLD, USO, SLV, EUR/USD (dropped Date, GLD target)
  - Y: GLD price

- **Train/Test Split:**
  - 80/20 split (random_state=2)

## 6. Model Training & Evaluation

- **Model:**
  - RandomForestRegressor (n_estimators=100)
    
- Trained on X_train/Y_train
  
- **Predictions:**
  - Generated test_data_prediction

- **Metrics:**
  - R² Score: Printed accuracy (typically ~98% for this dataset)
 
- **Visualization:**
  - Actual vs Predicted price line plot (blue actual, green predicted)

## 7. Tech Stack

- Python | Pandas | NumPy | Matplotlib | Seaborn | Scikit-learn (RandomForestRegressor, metrics.r2_score)


