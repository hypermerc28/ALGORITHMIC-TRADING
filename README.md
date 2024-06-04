Predictability of BBVA Stock Prices and Trading Volumes
Overview
This project aims to analyze and compare the predictability of BBVA stock prices and trading volumes using machine learning models. The study involves predicting the minute-by-minute returns and volumes for intraday data from 2014-2018, as well as daily returns and volumes for end-of-day data from Yahoo Finance spanning 2010-2023. The models used in this study are Random Forest Regressors.

Objectives
Calculate Returns:

Calculate minute-by-minute returns using the price data.
Calculate daily returns using end-of-day price data.
Handle Overnight Gaps:

Identify and handle overnight gaps in the intraday data to ensure accurate modeling.
Feature Engineering:

Create lagged features for both returns and volumes to capture temporal dependencies.
Model Training and Evaluation:

Train Random Forest models to predict minute-by-minute returns and volumes.
Train Random Forest models to predict daily returns and volumes.
Evaluate the models using RMSE (Root Mean Squared Error) and relative RMSE.
Dynamic Retraining:

Implement dynamic retraining to continuously update the models with new data points to maintain accuracy.
Dataset
Intraday Data: BBVA stock prices and volumes from 2014-2018 at 1-minute intervals.
End-of-Day Data: BBVA stock prices and volumes from Yahoo Finance for a period from 2010-2023.
Tools and Libraries
Programming Language: Python
Libraries:
pandas for data manipulation and analysis.
numpy for numerical computations.
matplotlib for data visualization.
sklearn for machine learning models and metrics.
yfinance for downloading financial data from Yahoo Finance.
Steps and Methodology
Data Loading and Inspection:

Load the intraday dataset and inspect its structure.
Combine 'date' and 'time' columns into a single 'Timestamp' column.
Calculating Returns:

Compute minute-by-minute returns for prices.
Compute daily returns for end-of-day prices.
Handling Overnight Gaps:

Identify overnight gaps by checking if the date changes from one row to the next.
Create a column 'Overnight' to mark these gaps.
Data Cleaning:

Remove rows with NA values resulting from return calculations.
Replace any infinite values with NaNs and drop them.
Feature Engineering:

Create lagged features for returns and volumes to use as predictors.
Model Training and Prediction:

Split the data into training and test sets (80% training, 20% testing).
Train Random Forest models on the intraday and end-of-day data.
Model Evaluation:

Evaluate the models using RMSE.
Plot predicted vs. actual returns and volumes to visually assess the model's accuracy.
Dynamic Retraining:

Implement dynamic retraining to update the models with new data points continuously.
Results and Comparison
The models' performance is evaluated using RMSE and relative RMSE.
The predictability of returns and volumes is compared using these metrics.
The visualizations show the actual vs. predicted returns and volumes for both intraday and daily data.
Conclusion
The study demonstrates the differences in predictability between BBVA stock prices and trading volumes. It highlights the challenges of predicting stock returns due to their inherent volatility compared to trading volumes.

