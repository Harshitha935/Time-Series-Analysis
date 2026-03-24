# 📱 iPhone Sales Forecasting

## 📌 Overview
This project develops a structured forecasting framework for iPhone unit sales by modeling two key drivers:

- 📈 Product lifecycle dynamics (launch spike → peak → decay)
- 📅 Calendar seasonality (annual/holiday effects)

Using historical data from iPhone 12–15, the models are trained and evaluated to predict future sales for newer generations (iPhone 16 and 17).

## 🧠 Key Ideas & Approach

Unlike simple time series models, this project decomposes sales into:

1. **Lifecycle Effects**  
   - Captures how sales evolve after product launch  
   - Models ramp-up, peak, and long-term decline  

2. **Seasonality**  
   - Uses sinusoidal features (sine/cosine) to model recurring yearly patterns  

3. **Cannibalization Effects**  
   - Accounts for competition between iPhone generations  

## 🚀 Models Implemented

### 🔹 Model 1: Ridge Regression (Baseline)
- Polynomial features to model lifecycle
- Normalized sales to handle scale differences
- Limitation: Overestimates early lifecycle sales due to peak normalization
- 
### 🔹 Model 2: Decomposed Model
- Separates:
  - Lifecycle structure
  - Seasonal variation
- Uses Ridge regression with engineered features:
  - `months_since_launch`
  - sine/cosine seasonal terms
- Improved performance and reduced overshooting

### 🔹 Model 3: Share-Based Model (Advanced)
- Predicts **sales share instead of absolute sales**
- Reduces complexity and better handles:
  - Demand shifts
  - Product competition
- Converts predicted share → actual sales using total yearly projections

## 📊 Data Processing
- Cleaned and standardized time-series data
- Generated key features:
  - `months_since_launch`
  - Model generation extraction
- Created panel dataset across models and time

## 📈 Results & Insights
- All iPhone models exhibit:
  - Strong launch spike followed by decay
  - Stable long-term sales levels
- Seasonality introduces predictable oscillations in sales
- Share-based modeling significantly improves forecast realism

## 🔮 Predictions
- Forecasted sales for:
  - iPhone 16 (validated with actual data)
  - iPhone 17 (forward-looking prediction)
- Demonstrates ability to generalize across product generations

## 🧰 Tech Stack
- Python
- Pandas & NumPy
- Scikit-learn (Ridge Regression, Pipelines)
- Matplotlib & Seaborn
