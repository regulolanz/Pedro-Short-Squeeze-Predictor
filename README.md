# Pedro Short Squeeze Predictor

## Table of Contents

- [Project Overview](#project-overview)
- [Concepts Review](#concepts-review)
- [Example](#example)
- [Installation and Usage](#installation-and-usage)
- [Data Prepation](#data-preparation)
- [Machine Learning Models](#machine-learning-models)
- [Results and Summary](#results-and-summary)
- [Analysis](#analysis)
- [Conclusion](#conclusion)

## Project Overview

Pedro is a machine learning project focused on predicting short squeezes in the stock market. By analyzing historical data on short float percentages and insider trading activity, Pedro aims to identify stocks with a high potential for rapid price increases. Leveraging various machine learning models, Pedro provides investors with insights to make informed trading decisions and take advantage of short squeeze opportunities in the market.

## Concepts Review

### Short Squeeze

- A short squeeze is a market phenomenon that occurs when a heavily shorted stock experiences a rapid increase in price. Short selling is a trading strategy where investors borrow shares of a stock and sell them, expecting the price to decline. They plan to buy back the shares at a lower price to return them to the lender and profit from the price difference.

- However, if the stock price starts to rise instead of falling, short sellers may panic and rush to buy back the shares to limit their losses. This increased demand for the stock can lead to a surge in its price, forcing more short sellers to cover their positions by buying shares. The buying pressure created by short sellers can amplify the upward movement of the stock, causing a short squeeze.

### Short Float 

- Short float, also known as short interest ratio, refers to the percentage of a company's outstanding shares that are held short by investors. It is a measure of the total number of shares sold short divided by the stock's total float (shares available for public trading). The float short ratio indicates the level of bearish sentiment in the market towards a particular stock. A higher float short ratio suggests a larger number of investors are betting against the stock, anticipating a price decline. This can potentially lead to a short squeeze if positive news or a significant price increase triggers a rush among short sellers to cover their positions, driving the stock's price higher.

### Insider Trading

- Insider trading refers to the buying or selling of stocks by individuals with access to non-public information. Insiders are legally required to disclose their trades to the regulatory authorities, such as the Securities and Exchange Commission (SEC) in the United States. The disclosed information typically includes the date of the trade, the number of shares bought or sold, and the price at which the transaction took place.

- Analyzing insider trading activity provides insights into the sentiment and confidence of insiders, large-scale insider buying may indicate that insiders believe the stock is undervalued and have positive expectations for its future performance.

## Example

#### AXDX Short Squeeze and Close-Up: 

![AXDX 30 Days](Resources/Images/AXDX_30D.png)![AXDX Closeup](Resources/Images/AXDX_closeup.png)

#### GRPN Short Squeeze and Close-Up: 

![GRPN 30 Days](Resources/Images/GRPN_30D.png)![GRPN Closeup](Resources/Images/GRPN_closeup.png)

#### SFIX Short Squeeze and Close-Up: 

![SFIX 30 Days](Resources/Images/SFIX_30D.png)![SFIX Closeup](Resources/Images/SFIX_closeup.png)
 
## Installation and Usage

1. Install the required libraries:

```bash
pip install numpy pandas yfinance tensorflow pandas_market_calendars scikit-learn imbalanced-learn
```

2. Clone the repository:

```bash
git clone https://github.com/regulolanz/Pedro-Short-Squeeze-Predictor
```

3. Run the project:

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

Pedro utilizes multiple machine learning models for predicting short squeezes. The selected models include GradientBoostingClassifier, SVC (Support Vector Classifier), RandomForestClassifier, DecisionTreeClassifier, and XGBClassifier.

#### GradientBoostingClassifier

The GradientBoostingClassifier is a machine learning model that builds an ensemble of weak prediction models, typically decision trees, to create a strong predictive model. It combines the predictions of multiple weak models to produce a final prediction.

#### SVC (Support Vector Classifier)

The SVC model is a supervised machine learning algorithm that separates data points into different classes using hyperplanes. It aims to find the best possible decision boundary that maximally separates the classes. 

#### RandomForestClassifier

The RandomForestClassifier is an ensemble learning model that combines multiple decision trees to make predictions. Each tree is trained on a subset of the data, and the final prediction is determined by a voting mechanism.

#### DecisionTreeClassifier

The DecisionTreeClassifier is a machine learning model that builds a decision tree based on the features of the data. It splits the data based on certain conditions at each node and makes predictions based on the majority class at the leaf nodes. 

#### XGBClassifier

The XGBClassifier is an implementation of the gradient boosting algorithm using decision trees as base learners. It is known for its efficiency and performance in handling complex datasets. 

## Results and Summary

- GradientBoostingClassifier:
    - Precision: 0.33
    - Recall: 0.33
    - F1-Score: 0.33
***
- SVC (Support Vector Classifier):
    - Precision: 0.00
    - Recall: 0.00
    - F1-Score: 0.00
***
- RandomForestClassifier:
    - Precision: 0.00
    - Recall: 0.00
    - F1-Score: 0.00
***
- DecisionTreeClassifier:
    - Precision: 0.20
    - Recall: 0.33
    - F1-Score: 0.25
***
- XGBClassifier:
    - Precision: 0.33
    - Recall: 0.33
    - F1-Score: 0.33
***
- Neural Network:
    - Precision: 0.00
    - Recall: 0.00
    - F1-Score: 0.00

## Analysis


## Conclusion

Pedro is a machine learning project that aims to predict short squeezes in the stock market by analyzing short float percentages and insider trading activity. By providing investors with insights and predictions, Pedro can help them make informed trading decisions and potentially take advantage of short squeeze opportunities. 