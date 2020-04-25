# Stock Market Analysis
Analyzing stock market trends using several different indicators in quantum finance. I explore machine learning and standard crossovers to predict future short term stock trends.

## Simple Analysis 

In quantum finance, the simplest of trading indicators is a crossover. A crossover is defined as when the short moving average crosses the long moving average, and a moving average is the average closing price over a set period. In this analysis, I utilize the Simple Moving Average and the Exponential Moving Average (which weighs newer averages greater). When our script detects a crossover in favor of the stock going up, a buy is triggered, and vice-versa for a sell. Using a custom backtesting analysis, we can test our strategy with historical data and even plot the trades. 
## Machine Learning

Our machine learning approach utilizes a vast set of indicators from the finta.py library. I utilize several complex moving averages, oscillators, strength indexes, and more. Other than that, our main data was aggregated using yahoo finance for every stock in the S&P500 for the past 30 years. In the Machine Learning folder, you can view a generated Jupyer Notebook pdf which goes into several different classification machine learning approaches. The variable I am trying to predict is called the short_result and is determined by the combined percent increase over 30 days over the S&P500. This is because a stock gaining 20% over 30 days is not impressive if the S&P500 increased by 30%. For example, if Apple's stock price increased 8% and the S&P500 dropped 2%, the short_result will be 10% and classified as a strong buy.

For the model and predictions on my [personal website](https://mathewsteininger.com/#stock), I utilized several AWS services, particularly SageMaker and Lambda do create an API for my models. SageMaker allowed me to easily tune and train multiple regression models with the optimal hyperparameters. Overall, the best model had a Mean Squared Error of around 28.5 and a Root Mean Squared Error of 5.3. This means that our validation tests differed on average from our model around 5%. The model on my website updates daily on the most current trading day's stocks for every S&P500 company.
## Installation

Stock Market Analysis requires python3 and pip

Install the requirements here
```
pip install -r requirements.txt
```


## Built With

* [Pandas](https://pandas.pydata.org) - Data Analysis Library
* [scikit-learn](https://scikit-learn.org/stable/) - Machine Learning Library


## Authors

* **Mat Steininger** - [Personal Site](https://mathewsteininger.com)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details