# Summary
This is the ridge regression model that my team and I built in 4 hours which was trained on over 1.1 million historical auction sale results, with over 50 product features, that enabled us to predict auction sale prices for heavy equipment better than the baseline predictor model by 16.5%. We came in 2nd place in the competition losing only slightly to the winning model.

# Description
The largest challenge of this project was the messy and sparse dataset. Therefore, we focused on engineering useful features and considering ways to deal with absent data. We determined that the following features were the most useful predictors:
- Equipment type
- Age
- Usage    

Given more time, we believe incorporating recent average prices by equipment type would also be a strong predictor of sale price.

`ridge_model.py` contains our error calculation, data processing pipeline, cross-validation and model training.

`run.py` and `score_model.py` are the code that were used to run and score our model.

# Contest Evaluation
The evaluation of our model was based on Root Mean Squared Log Error.
Which is computed as follows:

![Root Mean Squared Logarithmic Error](images/rmsle.png)

where *p<sub>i</sub>* are the predicted values and *a<sub>i</sub>* are the
target values.

Note that this loss function is sensitive to the *ratio* of predicted values to
the actual values, a prediction of 200 for an actual value of 100 contributes
approximately the same amount to the loss as a prediction of 2000 for an actual
value of 1000.  To convince yourself of this, recall that a difference of
logarithms is equal to a single logarithm of a ratio, and rewrite each summand
as a single logarithm of a ratio.

# Restrictions
The following techniques are legal

  - Linear Regression.
  - Logistic Regression.
  - Median Regression (linear regression by minimizing the sum of absolute deviations).
  - Any other [GLM](http://statsmodels.sourceforge.net/devel/glm.html).
  - Regularization: Ridge and LASSO.

You may use other models or algorithms as supplements (for example, in feature
engineering), but your final submissions must be scores from a linear type
model.
