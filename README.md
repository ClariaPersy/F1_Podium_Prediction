````markdown
# F1 Podium Prediction 

Predicts the top 3 drivers for upcoming F1 races using historical race data, qualifying times, driver form, and machine learning.

---

## Features
- Fetches past season F1 race data using **FastF1**
- Processes lap times, sector times, and driver stats
- Predicts race results using **XGBoost regression**
- Visualizes feature importance for predictions
- Optional: LLM-based explanations for podium predictions

---

## Requirements
- Python 3.9+
- fastf1
- pandas
- numpy
- scikit-learn
- xgboost
- matplotlib

Optional (if using LLM explanations):
- llama-index
- openai
- seaborn

Install dependencies via:

```bash
pip install -r requirements.txt
````

---

## Usage

1. Open `f1final.ipynb` in **Jupyter Notebook** or **Google Colab**.
2. Run all cells to:

   * Fetch and process historical race data
   * Train XGBoost regression model
   * Predict podium (top 3 drivers) for upcoming races
   * Display feature importance plots
3. View the predicted podium and optionally generate LLM explanations (requires API key).

---

## Notes

* Uses **FastF1 caching** to speed up repeated runs
* Predictions include adjustments for **driver form** and **starting grid advantage**
* Works with the last 2 seasons by default, but can be extended to more seasons

---

## File Structure

```
f1-podium-prediction/
├── f1final.ipynb       # Colab notebook with full model
├── README.md           # Project description
├── requirements.txt    # Dependencies
└── .gitignore          # Ignores cache, env, checkpoints, etc.
```

---

## How it Works

1. Fetch race and lap data for last 2 seasons using FastF1.
2. Process sector times and driver statistics.
3. Compute features: average FP times, qualifying times, driver form, team score, rain probability, temperature, etc.
4. Train XGBoost regression to predict race time.
5. Adjust predictions for **driver form dominance** and **starting grid advantage**.
6. Display top 3 predicted drivers and feature importance graph.

---

## Future Enhancements

* Integrate **real-time race data** for live predictions
* Add **LLM explanations** with OpenAI or Llama APIs
* Deploy as a **web app** for interactive usage
* Include **weather and tire strategy factors**

---

## License

MIT License – free to use, modify, and distribute.

---

Made with <3 by Claria Persy

```
