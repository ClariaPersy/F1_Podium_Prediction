# F1 Podium Prediction 

Predicts the top 3 drivers for upcoming F1 races using historical race data, qualifying times, driver form, and machine learning.

## Features
- Fetches past season F1 race data using FastF1
- Processes lap times, sector times, and driver stats
- Predicts race results using **XGBoost regression**
- Visualizes feature importance for predictions

## Requirements
- Python 3.9+
- fastf1
- pandas
- numpy
- scikit-learn
- xgboost
- matplotlib

Install dependencies via:
```bash
pip install -r requirements.txt
