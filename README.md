# Summary
Built a ridge regression model that was trained on over 1.1 million historical auction sale results, with over 50 product features, that enabled us to predict auction sale prices for heavy equipment 16.5% more accurately than the baseline predictor model.

# Methodology
EDA / Feature Engineering: The largest challenge of this project was the messy and sparse dataset. Therefore, we focused on engineering useful features and considering ways to deal with absent and incorrect data. We determined that the following features were the most useful predictors:
- Equipment type
- Age
- Usage    

Given more time, we believe incorporating recent average prices by equipment type would also be a strong predictor of sale price.


Model:
`ridge_model.py` contains our error calculation, data processing pipeline, cross-validation and model training.

`run.py` and `score_model.py` are the code that were used to run and score our model.

# Results
The evaluation of our model was based on Root Mean Squared Log Error.

![Root Mean Squared Logarithmic Error](images/rmsle.png)

Our final model predicted prices on held-out data 16.5% more accurately than the baseline weighted-average predictor model based on room mean squared log error.
