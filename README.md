# Pedro Short Squeeze Predictor

## Table of Contents

Pedro is a machine learning project focused on predicting short squeezes in the stock market. By analyzing historical data on short float percentages and insider trading activity, Pedro aims to identify stocks with a high potential for rapid price increases. Leveraging various machine learning models, Pedro provides investors with insights to make informed trading decisions and take advantage of short squeeze opportunities in the market.

## Table of Contents

- [Project Overview](#project-overview)
- [Installation and Usage](#installation-and-usage)
- [Data Prepation](#data-preparation)
- [Machine Learning Models](#machine-learning-models)
- [Results and Summary](#results-and-summary)
- [Analysis](#analysis)
- [Conclusion](#conclusion)

## Installation and Usage

1. Install the required libraries:

```bash
pip install numpy pandas yfinance tensorflow pandas_market_calendars scikit-learn imbalanced-learn
```

2. Clone the repository or download the Python script:

```bash
git clone https://github.com/regulolanz/Pedro-Short-Squeeze-Predictor
```

3. Run the code project:

```css
python Pedro.py
```

## Data Preparation

### Data Collection: 

Pedro gathers historical stock data, including short float percentages and insider trading data:

Short Data:

https://shortsqueeze.com/2023.php

Insider Trading:

https://github.com/JackLacey18/Insider-Trades

https://www.kaggle.com/datasets/jacklacey/insider-trades-for-1000-companies

https://www.insidermonkey.com/insider-trading/purchases/


Filters:
- Short Float = >17%
- Market Cap = >300M
- Insider Trading = >1M

### Data Processing:

The stock market data, float short, and insider trading data are combined based on the common stock ticker symbol or company identifier. Data cleaning and features engineering techniques are applied. This include handling missing values, normalizing or scaling features, encoding categorical variables, splitting the dataset into features and target variables. The features will include the selected columns from the previous step, while the target variable will be the 'Short Squeeze' column.

## Machine Learning Models: 

Pedro utilizes multiple machine learning models for predicting short squeezes. The selected models include:

- Feedforward Neural Network (FNN): A neural network model that can learn complex relationships between the input features and the target variable.

- Random Forest: An ensemble learning model that combines multiple decision trees to make predictions. It is known for handling non-linear relationships and capturing feature interactions.

- Oversampling with re-evaluation using Random Forest: To address class imbalance, Pedro applies the oversampling technique called Synthetic Minority Oversampling Technique (SMOTE) and re-evaluates the model's performance using the Random Forest algorithm.

## Results and Summary

Feedforward Neural Network (FNN):

- Test Accuracy: 85.71%
***

Random Forest:

- Original Data:
    - Precision: 1.00
    - Recall: 1.00
    - Specificity: 1.00
    - F1-Score: 1.00
    - Geometric Mean: 1.00
    - Index of Balanced Accuracy (IBA): 1.00
***

- Oversampled Data:
    - Precision: 0.92
    - Recall: 1.00
    - Specificity: 0.50
    - F1-Score: 0.96
    - Geometric Mean: 0.71
    - Index of Balanced Accuracy (IBA): 0.53

## Analysis

The FNN model achieved a test accuracy of 85.71%, indicating its ability to predict short squeezes with a good level of accuracy.

The Random Forest model, trained on the original data, demonstrated perfect performance with precision, recall, specificity, F1-score, geometric mean, and IBA all equal to 1.00. This suggests that the model accurately identified short squeeze opportunities in the original dataset.

Based on the evaluation results, it can be observed that oversampling the data improved the performance of the Random Forest model in terms of overall metrics, such as precision, recall, F1-score, and geometric mean. However, it's important to note that oversampling can introduce some trade-offs and potential challenges.

When oversampling was applied to address class imbalance, the performance of the Random Forest model on the oversampled data showed slightly different results. The precision decreased to 0.92, while recall remained at 1.00. The specificity decreased to 0.50, indicating a higher rate of false positives. The F1-score and geometric mean were still high at 0.96 and 0.71, respectively. The IBA decreased to 0.53, reflecting the impact of oversampling on the model's performance.

## Conclusion

Pedro is a machine learning project that aims to predict short squeezes in the stock market by analyzing short float percentages and insider trading activity. By providing investors with insights and predictions, Pedro can help them make informed trading decisions and potentially take advantage of short squeeze opportunities. 