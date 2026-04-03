📱 iPhone Sales Forecasting
📌 Overview

Built a forecasting model for iPhone sales by modeling product lifecycle and seasonality, using historical data from iPhone 12–15 to predict demand for iPhone 16 and 17.

📊 Key Results
Improved MAE from 0.115 → 0.073 (+36.6% vs baseline)
Validated model on unseen iPhone 16 data
Generated forward-looking forecasts for iPhone 17

🧠 What I Did
Engineered lifecycle features (months_since_launch) to model product adoption and decay
Captured seasonality using sine/cosine encoding
Built multiple models (baseline → improved → share-based) using Ridge Regression
Structured data across product generations for cross-model learning
🛠 Tech Stack

Python, Pandas, NumPy, Scikit-learn, Matplotlib

💡 Key Insight

Explicitly modeling lifecycle + seasonality significantly improves forecast accuracy and generalization across product generations
