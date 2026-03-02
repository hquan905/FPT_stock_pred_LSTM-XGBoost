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

The models were evaluated using MAE, MSE and R² score on both training and testing datasets

* **LSTM**

  -MAE:	0.05

  -RMSE:	0.05

  -R²:	0.79

* **Hybrid LSTM + XGBoost**
  
  -MAE: 0.01
  
  -RMSW: 0.02
  
  -R²:	0.98

** Key Findings **

The hybrid model reduced RMSE from 0.05 to 0.02 (~60% improvement).

R² improved significantly from 0.79 to 0.98, indicating much stronger explanatory power.

Residual learning with XGBoost substantially improved prediction accuracy.

The hybrid model better handled nonlinear fluctuations and short-term volatility.

** Conclusion **

This project demonstrates that combining deep learning and gradient boosting significantly enhances financial time-series forecasting performance.

While LSTM effectively captures trend and sequential dependencies, it struggles with nonlinear shocks and abrupt market movements. By training XGBoost on residual errors, the hybrid model successfully corrects systematic prediction bias and improves generalization on unseen data.

The results confirm that residual learning is a powerful strategy for improving forecasting robustness in financial markets.
