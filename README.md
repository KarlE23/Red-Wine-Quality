# Red Wine Quality – Modeling Summary

In this project, I created three models using the winequality-red.csv dataset from Kaggle, applying a 70/30 train-test split throughout. Two regression models were built in Azure Machine Learning Studio, and one classification model was developed using Python.

Single-Feature Regression Model (Citric Acid → Alcohol):
I used citric acid to predict alcohol content using linear regression. The model showed poor performance, with a MAE of 0.84, RMSE of 1.02, and R² of just 1.4%. This suggests a weak and likely non-linear relationship between citric acid and alcohol level.

Multi-Feature Regression Model (Chlorides, pH, Sulphates → Alcohol):
Using three predictors, the multiple linear regression model slightly improved results: MAE of 0.796, RMSE of 0.977, and R² of 9.3%. Despite the improvement, the model still performed poorly, indicating that the chosen features lack strong predictive power for alcohol content.

Classification Model (Predicting Wine Quality – High vs. Low):
A logistic regression model was built in Python using 5 features (alcohol, chlorides, pH, sulphates, density). I transformed the quality column into binary classes (low = 0–5, high = 6–10). The model achieved an accuracy of 73.3%, with F1-scores of 75% (high) and 72% (low). The confusion matrix and classification report indicated balanced performance with moderate precision and recall.

Conclusion:
The classification model yielded the best results, providing reasonable accuracy in distinguishing wine quality. The regression models performed poorly, especially when using a single feature. Future work should consider feature engineering or alternative algorithms to improve predictive accuracy.
