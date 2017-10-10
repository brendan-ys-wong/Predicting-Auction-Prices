# Regression model for predicting auction prices  
This is the ridge regression model my team and I built that was trained on over 1.1 million historical auction sale results, with over 50 product features, which enabled us to predict auction sale prices for heavy equipment 16.5% better than the baseline predictor model.

## Description
The largest challenge of this project was messy and sparse data. Therefore, we focused on engineering useful features and considering ways to deal with absent data. We determined that the following features were the most useful predictors:
- Equipment type
- Age
- Usage
Given more time, we believe incorporating recent average prices by equipment type would also be a strong predictor of sale price.

`ridge_model.py` contains our error calculation, data processing pipeline, cross-validation and model training.

`run.py` and `score_model.py` are the code that run and score our model.
