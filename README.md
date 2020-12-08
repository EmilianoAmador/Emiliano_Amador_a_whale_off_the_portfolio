# Algorithmic Trading Strategies: Comparing Whale Portfolio's With Python and Pandas

![Portfolio Analysis](Images/portfolio-analysis.png)

## Introduction

In this quantitative analysis file, I used Python and Pandas to evaluate six major investment portfolios accross various metrics to see which portfolio outperforms the rest. To do this, I created a tool that analyzes and visually organizes each portfolio's volatility, risk, returns, and sharpe ratios using their historical daily returns. The portfolios evaluated include the distinguished Berkshire Hathaway portfolio, two algorithmic portfolios from an undisclosed trading firm (Algo 1 and Algo 2), and three portfolios from hedge and mutual funds firms. The historical data was provided by yahoo finance and placed into csv files using excel.

Lastly, I used the results from the portfolio analysis to create a custom stocks portfolio and ran it against the other portfolios as well as the S&P 500. 

1. [Read in and Wrangle Returns Data](#Prepare-the-Data)
2. [Determined Success of Each Portfolio](#Conduct-Quantitative-Analysis)
3. [Created and Evaluatde a Custom Portfolio](#Create-Custom-Portfolio)

---


### Preparing the Data

First, read and cleaned several CSV files for analysis. The CSV files include whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. [Whale Analysis](whale_analysis.ipynb)

1. Imported each of the CSV files as a DataFrame.

2. Detected and remove null values.

3. Removed signs from the numeric values and converted the data types where needed.

4. Converted the S&P 500 closing prices to daily returns to match with the whale portfolios and the algorithmic portfolios.

5. Joined all the portfolios into a single DataFrame with columns for each portfolio's returns.

  ![returns-dataframe.png](Images/returns-dataframe.png)

### Conducted Quantitative Analysis

Analyze the data to see if any of the portfolios outperform the stock market (i.e., the S&P 500).

#### Performance Analysis

1. Cumulative returns. Does any portfolio outperform the S&P 500?

#### Risk Analysis

1. Create a box plot for each of the returns. Which box has the largest spread? Which has the smallest spread?

2. Calculate the standard deviation for each portfolio. Which portfolios are riskier than the S&P 500?

#### Rolling Statistics

1. Plot the rolling standard deviation of the firm's portfolios along with the rolling standard deviation of the S&P 500. Does the risk increase for each of the portfolios at the same time risk increases in the S&P?

2. Construct a correlation table for the algorithmic, whale, and S&P 500 returns. Which returns most closely mimic the S&P?

3. Choose one portfolio and plot a rolling beta between that portfolio's returns and S&P 500 returns. Does the portfolio seem sensitive to movements in the S&P 500?

### Plot Sharpe Ratios

Investment managers and their institutional investors look at the return-to-risk ratio, not just the returns. (After all, if you have two portfolios that each offer a 10% return, yet one is lower risk, you would invest in the lower-risk portfolio, right?)

1. Using the daily returns, calculate and visualize the Sharpe ratios using a bar plot.

2. Determine whether the algorithmic strategies outperform both the market (S&P 500) and the whales portfolios.

### Create Custom Portfolio

Harold is ecstatic that you were able to help him prove that the algorithmic trading portfolios are doing so well compared to the market and whales portfolios. However, now you are wondering whether you can choose your own portfolio that performs just as well as the algorithmic portfolios. Investigate by doing the following:

1. Visit [Google Sheets](https://docs.google.com/spreadsheets/) and use the in-built Google Finance function to choose 3-5 stocks for your own portfolio.

2. Download the data as CSV files and calculate the portfolio returns.

3. Add your portfolio returns to the DataFrame with the other portfolios and rerun the analysis. How does your portfolio fair?

---

## Resources

[Pandas API Docs](https://pandas.pydata.org/pandas-docs/stable/reference/index.html)
