# Freight Rate Prediction Report

## 1. Objective

Build a regression model that predicts posted freight rates from historical shipment data.

## 2. Data

Describe the 48,000 training rows, the 12,000 final validation rows, the date ranges, the target, and the main input features.

## 3. Data quality

Mention missing weight and market_index values and the negative weight values. Explain the chosen treatment.

## 4. Feature engineering

Describe route, date features, log transformations, distance per 1,000 lb, and coordinate gap.

## 5. Validation strategy

Explain the January-September training period and October holdout. Explain why a time-based split was used.

## 6. Model

Describe CatBoostRegressor, categorical features, MAE loss, early stopping and the final number of iterations.

## 7. Validation results

Copy the MAE and RMSE printed by the notebook.

## 8. December prediction chart

Insert `scorer_results/candidate_december.png`.

## 9. Final output

Mention that `validation_predictions.csv` contains 12,000 rows with `load_id` and `predicted_rate`.
