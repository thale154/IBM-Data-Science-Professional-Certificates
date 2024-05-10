# Project Overview

For this project, you will assume the role of a Data Scientist / Data Analyst working for a new startup investment firm that helps customers invest their money in stocks. Your job is to extract financial data like historical share price and quarterly revenue reportings from various sources using Python libraries and webscraping on popular stocks. After collecting this data you will visualize it in a dashboard to identify patterns or trends. The stocks we will work with are Tesla, Amazon, AMD, and GameStop.

## Dashboard Analytics Displayed

A dashboard often provides a view of key performance indicators in a clear way. Analyzing a data set and extracting key performance indicators will be practiced. Prompts will be used to support learning in accessing and displaying data in dashboards. Learning how to display key performance indicators on a dashboard will be included in this assignment. We will be using Plotly in this course for data visualization and is not a requirement to take this course.

In the Python for Data Science, AI and Development course you utilized Skills Network Labs for hands-on labs.

For this project you will use Skills Network Labs and Watson Studio. Skills Network Labs is a sandbox environment for learning and completing labs in courses. Whereas Watson Studio, a component of IBM Cloud Pak for Data, is a suite of tools and a collaborative environment for data scientists, data analysts, AI and machine learning engineers and domain experts to develop and deploy your projects.

## Review criteria

There are two hands-on labs on Extracting Stock Data and one assignment to complete. You will be judged by completing two quizzes and one peer review assignment. The quizzes will test you based on the output of the hands-on labs. In the peer review assignment you will share and take screen shots of the outcomes of your assignment.

# Stock shares

A company's stock share is a piece of the company; more precisely:

A stock (also known as equity) is a security that represents the ownership of a fraction of a corporation. This entitles the owner of the stock to a proportion of the corporation's assets and profits equal to how much stock they own. Units of stock are called "shares."

An investor can buy a stock and sell it later. If the stock price increases, the investor profits, If it decreases,
the investor with incur a loss. Determining the stock price is complex; it depends on the number of outstanding shares, the size of the company's future profits, and much more. People trade stocks throughout the day. The stock ticker is a report of the price of a certain stock, updated continuously throughout the trading session by the various stock market exchanges. In this lab, you will use the y-finance API to obtain the stock ticker and extract information about the stock. You will then be asked questions about your results.

# Extracting Stock Data Using a Python Library

In this lab, you will use a Python library to obtain financial data. You will extract historical stock data using **yfinance**. A graded quiz will follow to test you on the results in the lab.

To complete this lab you will utilize JupyterLab running on the Cloud in Skills Network Labs environment. To launch the lab notebook in a new browser tab check the box below and click on the "Launch App" button.

# The yfinance Python library

The yfinance is a Python library with a user-friendly interface for downloading historical market data from Yahoo Finance. It lets you get historical stock prices, dividends, and other financial data for stocks, exchange-traded funds (ETFs), and other securities.

This example shows code for using yfinance to download historical stock prices.

```python
import yfinance as yf

# Download historical data for a stock
msft = yf.Ticker("MSFT")
msft_data = msft.history(period="max")

# Display the downloaded data
msft_data.head()
```

Explanation for the above code:

First, import the yfinance library using the alias yf.
Then, create a Ticker object for the Microsoft stock (“MSFT”).
Use the history method of the Ticker object to download the historical data for the stock. The period parameter of the history method specifies when you want to download the data. In this example, it is set to max to download the maximum available historical data.

Here are some of the possible values for the period parameter and what they represent:

- period="1d": Download 1 day of historical data.
- period="5d": Download 5 days of historical data.
- period="1mo": Download 1 month of historical data.
- period="3mo": Download 3 months of historical data.
- period="6mo": Download 6 months of historical data.
- period="1y": Download 1 year of historical data.
- period="2y": Download 2 years of historical data.
- period="5y": Download 5 years of historical data.
- period="10y": Download 10 years of historical data.
- period="ytd": Download historical data since the beginning of the current year.
- period="max": Download all available historical data.

Finally, you print the downloaded data using the head function. This downloaded data will display a Pandas data frame containing Microsoft's historical stock prices and other financial data.
