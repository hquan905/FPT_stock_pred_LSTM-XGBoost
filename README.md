# FPT Stock Price Prediction: Hybrid LSTM-XGBoost Model

## Overview
This project develops a hybrid time-series forecasting model to predict the stock price of FPT by combining Deep Learning and Gradient Boosting techniques.

Instead of relying on a single model, this approach decomposes the prediction problem into:

LSTM → Captures temporal structure, overall trend, and short-term mean reversion

XGBoost → Learns residual errors from LSTM to capture nonlinear patterns and sudden market shocks

Final prediction:
Final Prediction=LSTM Prediction+XGBoost Residual Prediction

This hybrid architecture improves robustness and reduces forecast error compared to standalone models.

## Project Structure

- `BaoCaoDubao_FPT.pdf`  
  Detailed project report (Vietnamese) covering methodology, theoretical background, model design, and evaluation results.

- `FPT_stock_pred.ipynb`  
  Main Jupyter Notebook including:
  - Data preprocessing
  - Feature engineering
  - LSTM model training
  - Residual learning with XGBoost
  - Model evaluation and visualization

- `requirements.txt`  
  List of required Python dependencies.
  
## Dataset

* **Source:** Investing.com
* **Ticker:** FPT.
* **Timeframe:** 02/03/2016 - 02/03/2026.
* **Target Variable:** Close Price.
  
## Results & Conclusion

