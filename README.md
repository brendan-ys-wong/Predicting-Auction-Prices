# Regression model for predicting auction prices for heavy equipment

My team and I built a ridge regression model that analyzed over 1.1 million historical auction sale results, with 50+ product features, which enabled us to predict auction sale prices for unseen products 16.5% better than the baseline predictor.

_Description_
The largest challenge of this project was messy and sparse data. Therefore, we focused on engineering useful features and considering ways to deal with absent data.

We determined that a combination of equipment type, age, and usage were the strongest variables predicting sale price.
Given more time, we believe recent average prices by equipment type would also be a strong predictor of sale price.

ridge_model.py contains our error calculation, data processing pipeline, cross-validation and model training.

run.py and score_model.py run our script and score our model.
