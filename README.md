# Uncovering Donation Patterns: Predictive Analytics for Regional Charity Impact

## Summary
This project explores and predicts regional donation and project trends using open charity data from ``Eid Charity``

The goal is to **reveal when, where, and how donations happen**, and to test forecasting models that can support social impact campaigns. This is helpful for organizations such as ``Eid Charity``, ``Giving Tuesday``, etc.


## Key steps completed
- **Data Wrangling** → Cleaning, feature engineering, and handling inconsistencies.  
- **Data Exploration & Visualization** → Identifying geographical and temporal trends, including tools like ``Pareto charts``.
- **Time-Series Analysis** → Detecting seasonality and donation cycles.  
- **Forecasting (SARIMA)** → Predicting future donation volumes and values.  
- **Social Insights** → Linking donation spikes to cultural and religious events.  


---

## Repository content
- `README.md` → This documentation.  
- `conda_environment.yml` → Conda environment file with all required libraries.  
- `eda_and_timeseries_forecast.ipynb` → Main notebook with analysis, visualizations, and forecasting models.  
- ``*Dataset``: *EID Charity Main Data File.csv* → Not included in this repository due to size restrictions.  
  - You can download it directly from Kaggle: [Eid Charity Dataset](https://www.kaggle.com/datasets/rolanddecker/hundeyin-charity-dataset?select=EID+Charity+Main+Data+File.csv)  
  - Once downloaded, place it in the project root directory before running the notebook. 

## Installation and Reproducibility
1. Clone this repository
2. Create the environment with Conda from the environment.yml file:
```
    conda env create -f environment.yml
    conda activate global_charity_analytics
```
3. Open the notebook: `eda_and_timeseries_forecast.ipynb`

---

## Key Insights
1. **Most projects are low-cost** (<5,000 USD), but a few very large donations (top 30%) skew the average.
2. **Seasonality is strong**: donations spike during ``Ramadan``, reflecting cultural and religious giving traditions.
3. **Projects ≠ Donations**: the countries with the most projects are not always the ones receiving the highest funding.
4. **Forecasting accuracy**:
- Number of projects → MAPE ≈ 16.1% (good accuracy for real-world data).
- Value of donations → MAPE ≈ 18.8% when excluding extreme outliers.

## Impact and Contribution
This analysis shows how historical data can help:
- Understand regional giving behaviors.
- Identify the best times of year to launch donation campaigns.
- Predict funding trends and maximize social impact.

---

## Limitations
- Data consistency is ``reliable only from 2008–2016``, reducing usable training data.
- Donations are ``highly volatile`` (outliers), making predictions harder for very large contributions.

## Next steps
- Refine models with more historical data.
- Incorporate ``external`` variables (religious holidays, global campaigns).
- Evaluate alternative models such as ``Prophet`` or ``XGBoost`` for more robust predictions.
