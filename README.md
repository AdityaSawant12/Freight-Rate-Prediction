# Freight Rate Prediction

This project builds a regression model to predict freight load posted rates.

## Dataset

- `data/train_test.csv` - 48,000 labeled loads from January to October 2025
- `data/validation.csv` - 12,000 loads from November and December 2025
- `data/december_chart_inputs.csv` - 31 fixed December test cases
- `data/validation_predictions_template.csv` - required output format

## Notebook

Open `freight_rate_prediction.ipynb` and run the cells from top to bottom.

The notebook:

1. Loads and checks the data
2. Looks at missing values and unusual weights
3. Creates route and date features
4. Uses October 2025 as a time-based validation period
5. Trains a CatBoost regression model
6. Reports MAE and RMSE
7. Retrains the model on all labeled data
8. Creates `validation_predictions.csv`
9. Creates December predictions
10. Runs the provided scorer

## Install

```bash
pip install -r requirements.txt
```

## Output

After the notebook is run:

- `validation_predictions.csv`
- `data/december_chart_inputs.csv` with predictions filled in
- `scorer_results/candidate_december.png`

The required validation output has exactly these columns:

```text
load_id,predicted_rate
```

## Notes

The final competition metric is calculated by Spotter after submission. The notebook uses October as a holdout period because the final validation data is later in time.
