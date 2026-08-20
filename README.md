# HDB Resale Price Prediction

**Student:** Tan Hui Kiang (Judy)
**Student ID:** 4061218C  
**Module:** ITD224  
**Project:** Final Individual Project Portfolio  

## Business Problem

HDB buyers, sellers and property professionals require reliable resale
price estimates to support pricing and purchasing decisions. This project
uses historical HDB resale transactions to identify major price drivers
and build regression models that predict resale prices.

## Project Objectives

- Clean and prepare the HDB resale transaction dataset.
- Perform professional exploratory data analysis.
- Engineer meaningful time, lease, age and storey features.
- Compare at least three regression models.
- Evaluate the models using MAE, RMSE and R².
- Identify important price drivers.
- Provide practical recommendations.

## Dataset

The project uses HDB resale transaction data covering January 2017 to
July 2026. The data source and access instructions are documented in
[data/README.md](data/README.md).

## CRISP-DM Workflow

1. Business Understanding
2. Data Understanding
3. Data Preparation
4. Modelling
5. Evaluation
6. Deployment Recommendations

## Evidence of Individual Contribution

The following table summarises my individual technical and business contributions to this project. Supporting evidence is available in the final Jupyter Notebook, portfolio report and selected visualisations.

| Competency | Individual Contribution | Evidence |
|---|---|---|
| Data Preparation | Removed duplicate records, corrected data types, handled missing or invalid values, validated transaction fields, transformed variables and exported the cleaned dataset. | [Final Notebook](4061218C_ITD224_Final_DataCleaning_EDA_Modelling_Evaluation.ipynb) |
| Feature Engineering | Created remaining lease years, resale year and month, flat age, storey midpoint and outlier indicators for analysis and modelling. | [Final Notebook](4061218C_ITD224_Final_DataCleaning_EDA_Modelling_Evaluation.ipynb) |
| Exploratory Data Analysis | Analysed resale-price trends, towns, flat types, price distributions, remaining lease, scatterplots, boxplots and correlations. | [EDA Figures](images/) |
| Modelling | Developed and compared three regression pipelines using a chronological train-test split and hyperparameter comparison. | [Final Notebook](4061218C_ITD224_Final_DataCleaning_EDA_Modelling_Evaluation.ipynb) |
| Evaluation | Evaluated models using MAE, RMSE and R², together with residual analysis, segment performance and feature importance. | [Model Evaluation Figures](images/) |
| Business Communication | Assessed whether the final model met the business objective and presented recommendations, limitations and a proposed deployment workflow. | [Portfolio Report](4061218C_ITD224_Final_Project_Portfolio_Report.pdf) |

## Models Evaluated

- Linear Regression
- Decision Tree Regressor
- Random Forest Regressor
- Additional tuned model, where applicable

## Model Performance Results

| Model | Evaluation Period | MAE (S$) | RMSE (S$) | R² |
|---|---|---:|---:|---:|
| Ridge Regression | 2025 validation | 62,142.20 | 87,644.04 | 0.816 |
| Random Forest | 2025 validation | 51,564.48 | 73,481.21 | 0.870 |
| Histogram Gradient Boosting | 2025 validation | 50,942.05 | 69,119.16 | 0.885 |
| Final Tuned Histogram Gradient Boosting | 2026 test | 37,274.69 | 53,549.33 | 0.937 |

## Interpretation
The initial models were compared using the 2025 validation dataset. Histogram
Gradient Boosting achieved the strongest initial performance, with the lowest
RMSE of S$69,119.16 and the highest R² of 0.885.

After hyperparameter tuning, the final Histogram Gradient Boosting model was
retrained using transactions from 2017 to 2025 and evaluated on the untouched
2026 test dataset. It achieved an MAE of S$37,274.69, an RMSE of S$53,549.33
and an R² of 0.937. This means that the final model explained approximately
93.7% of the variation in 2026 HDB resale prices.

## Selected Visualizations

![HDB price trend](images/01_price_trend.png)

![Average price by town](images/02_average_price_by_town.png)

![Correlation heatmap](images/03_correlation_heatmap.png)

## How to Run the Project

1. Download or clone this repository.
2. Install the required packages:

   `pip install -r requirements.txt`

3. Obtain the dataset using the instructions in `data/README.md`.
4. Place the dataset in the expected data location.
5. Open the final Jupyter Notebook.
6. Run all cells from top to bottom.

## Repository Contents

- Final Jupyter Notebook – complete reproducible workflow
- Portfolio report – project explanation and findings
- `data/README.md` – dataset source and access instructions
- `images/` – selected project visualisations
- `requirements.txt` – required Python packages
- `RESPONSIBLE_USE.md` – responsible-use and limitations statement

## Limitations and Future Improvements

The model is based on historical transactions and may not account for
renovation quality, exact block location, nearby facilities or unexpected
market changes. Future work could include geospatial features, amenity
distances, more advanced models and periodic model retraining.

## My individual contribution for HDB resale-price prediction workflow included:

1. Cleaning and validating the HDB resale transaction dataset.
2. Converting variables into appropriate data types.
3. Removing duplicate and invalid records.
4. Engineering time, lease, flat-age and storey features.
5. Conducting exploratory data analysis and preparing visualisations.
6. Developing and comparing at least three regression pipelines.
7. Applying a chronological train-test split to reduce data leakage.
8. Tuning the strongest-performing model.
9. Evaluating model performance using MAE, RMSE and R².
10. Interpreting residuals, segment results and feature importance.
11. Assessing whether the model achieved the business objective.
12. Preparing recommendations, limitations and deployment considerations.

The final notebook provides the reproducible technical workflow, while the portfolio report explains the findings and business implications.
