# Pedro_Data

1. **Functionality:** The code appears to be designed to ingest and process stock market data from CSV files. It specifically focuses on short float and insider trading data to predict potential short squeezes. After cleaning and merging the datasets, it creates several new features, computes returns for different time intervals, and determines if a short squeeze occurred based on these returns. Finally, it saves the resulting dataframe into a CSV file. This functionality seems to be in order.

2. **Code Organization:** Your code is well-structured with comments, constant declarations, and defined functions, which make it easier for others to read and understand.

3. **Data Preprocessing:** Your data cleaning and preprocessing look comprehensive. You handle different data types and inconsistencies in your data well.

4. **Feature Engineering:** You use both stock data and date information to create new features. You've also set up rules to identify short squeezes based on the returns for different time intervals. This looks good.

5. **Dependencies:** You are importing and using appropriate libraries for data manipulation (pandas, numpy), data extraction (yfinance), and date handling (pandas_market_calendars).

# Pedro_Model

1. **Import Libraries:** Various libraries are imported such as numpy, pandas, matplotlib, xgboost, tensorflow, sklearn, imblearn, etc.

2. **Data Import:** The data is read from a CSV file named "ShortSqueezeData.csv".

3. **Data Cleaning:** The data is checked for the number of instances for "Short Squeeze" and "Non Short Squeeze".

4. **Data Visualization:** Visual representations are created using the matplotlib library, such as the number of short squeezes by sector and year.

5. **One Hot Encoding:** One-hot encoding is used to convert categorical variables into a form that could be provided to machine learning algorithms to improve their performance.

6. **Train-Test Split:** The data is divided into a set of training data and a set of test data. The model will be trained on the training data and its performance will be evaluated on the test data.

7. **Data Normalization:** Standard Scaler from sklearn is used to normalize the data. Normalization is important in machine learning because it makes all features to contribute equally regardless of their scale.

6. **Class Balancing:** The Synthetic Minority Over-sampling Technique (SMOTE) is used to balance the classes in the dataset. SMOTE works by creating synthetic samples from the minor class instead of creating copies, which makes the classifier less prone to overfitting.

7. **Model Training:** Various machine learning models (like Gradient Boosting, Support Vector Machines, Random Forest, Decision Trees, XGBoost, and Neural Networks) are trained on the balanced and scaled training data and then evaluated on the scaled test data.

--

A **confusion matrix** is a table that is often used to describe the performance of a classification model on a set of test data for which the true values are known. It allows you to visualize the performance of a classification algorithm by displaying the counts of true positive, true negative, false positive, and false negative predictions.

Here's a breakdown of the elements in a confusion matrix:

- True Positive (TP): The model correctly predicted the positive class.
- True Negative (TN): The model correctly predicted the negative class.
- False Positive (FP): The model incorrectly predicted the positive class when the actual class was negative (Type I error).
- False Negative (FN): The model incorrectly predicted the negative class when the actual class was positive (Type II error).

The confusion matrix is often visualized using a heatmap, where the cells represent the counts or proportions of the predicted labels. The diagonal cells (top-left to bottom-right) represent the correct predictions, while the off-diagonal cells represent the incorrect predictions.

The visualization helps you quickly assess the model's performance by looking at the distribution of the predicted labels compared to the actual labels. You can see how well the model is classifying the positive and negative examples based on the distribution of the counts in each cell.

