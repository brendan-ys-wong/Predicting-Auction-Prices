# Regression model for predicting auction prices  
This is the ridge regression model that my team and I built which was trained on over 1.1 million historical auction sale results, with over 50 product features, that enabled us to predict auction sale prices for heavy equipment better than the baseline predictor model by 16.5%.

## Description
The largest challenge of this project was the messy and sparse dataset. Therefore, we focused on engineering useful features and considering ways to deal with absent data. We determined that the following features were the most useful predictors:
- Equipment type
- Age
- Usage    
  
Given more time, we believe incorporating recent average prices by equipment type would also be a strong predictor of sale price.

`ridge_model.py` contains our error calculation, data processing pipeline, cross-validation and model training.

`run.py` and `score_model.py` are the code that were used to run and score our model.
