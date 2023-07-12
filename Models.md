# Models

## Gradient Boosting Classifier
These are often among the best performers for tabular data (like the one you're using), but they require careful tuning and can be prone to overfitting if not properly regularized.

**Classification Report**

       precision    recall  f1-score   support
       
           0       0.75      0.86      0.80         7
           1       0.50      0.33      0.40         3

    accuracy                           0.70        10
   macro avg       0.62      0.60      0.60        10
weighted avg       0.68      0.70      0.68        10


## Support Vector Machine (SVM)
SVMs can be quite powerful for certain datasets, especially if the data is not linearly separable. However, they can be sensitive to overfitting on noisy datasets and can be computationally intensive for larger datasets.

**Classification Report**

       precision    recall  f1-score   support
       
           0       0.62      0.71      0.67         7
           1       0.00      0.00      0.00         3

    accuracy                           0.50        10
   macro avg       0.31      0.36      0.33        10
weighted avg       0.44      0.50      0.47        10


## Random Forest 
An ensemble of Decision Trees, Random Forests are generally more accurate than individual trees but can be harder to interpret. They handle feature interactions well and are less prone to overfitting.

**Classification Report**

       precision    recall  f1-score   support
       
           0       0.67      0.86      0.75         7
           1       0.00      0.00      0.00         3

    accuracy                           0.60        10
   macro avg       0.33      0.43      0.38        10
weighted avg       0.47      0.60      0.53        10


## Decision Tree Classifier
This type of model is also interpretable and can capture non-linear relationships. However, it tends to overfit if not properly tuned.

**Classification Report**

       precision    recall  f1-score   support

           0       0.57      0.57      0.57         7
           1       0.00      0.00      0.00         3

    accuracy                           0.40        10
   macro avg       0.29      0.29      0.29        10
weighted avg       0.40      0.40      0.40        10


## Feedforward Neural Network (FNN)

**Classification Report**

 precision    recall  f1-score   support

           0       0.62      0.71      0.67         7
           1       0.00      0.00      0.00         3

    accuracy                           0.50        10
   macro avg       0.31      0.36      0.33        10
weighted avg       0.44      0.50      0.47        10

