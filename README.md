# Algorithmic Trading
## 1. Equal-Weight S&P 500 Screener
## 2. Quantitive Momentum Screener
## 3. Quantitive Value Screener

## Introduction

Algorithmic trading refers to the use of computer programs or algorithms to execute trading strategies in financial markets. These algorithms use mathematical models and statistical analysis to identify profitable trading opportunities and to make buy or sell decisions based on pre-defined rules.

The algorithms can be designed to trade in various financial instruments, such as stocks, options, futures, and currencies, and can be programmed to execute trades automatically without any human intervention. Algorithmic trading is often used by large institutional investors, such as hedge funds and investment banks, but it is becoming increasingly popular among retail traders as well.

Algorithmic trading has several advantages over traditional manual trading, including faster and more efficient execution of trades, the ability to process large amounts of data and make decisions based on it, and the ability to backtest and optimize trading strategies using historical data. However, algorithmic trading also carries some risks, such as the possibility of technical glitches or market volatility that can cause unexpected losses.

### Equal-Weight S&P 500

The S&P 500 is a stock market index that tracks the performance of 500 large-cap U.S. companies listed on major stock exchanges. There are two main ways that the S&P 500 can be weighted: equal-weighted and capitalization-weighted.

Capitalization-weighted, also known as market-cap weighted, means that each company's weight in the index is proportional to its market capitalization, which is calculated by multiplying the company's stock price by the number of outstanding shares. This means that the largest companies in the index, such as Apple, Microsoft, and Amazon, have a larger impact on the index's performance than smaller companies.

On the other hand, equal-weighted means that each company in the index has an equal weight, regardless of its market capitalization. This means that smaller companies have the same impact on the index's performance as larger companies.

For example, if the S&P 500 was equally-weighted, each of the 500 companies would have a weight of 0.2% (1/500), while under a capitalization-weighted index, the largest companies may have a weight of several percentage points.

Equal-weighted indexes tend to have higher exposure to smaller companies and can provide a more diversified exposure to the market, while capitalization-weighted indexes are more concentrated in larger companies that are typically more established and stable.

### Stock Portfolio Optimizer
This project is a stock portfolio optimizer that retrieves the latest price and market capitalization data of the S&P 500 stocks from the IEX Cloud API, and calculates the number of shares to buy for each stock to create an equally-weighted portfolio.

### Requirements
- Python 3.6 or higher
- numpy 1.20.1 or higher
- pandas 1.2.2 or higher
- requests 2.25.1 or higher
- xlsxwriter 1.3.7 or higher
- IEX Cloud API key (saved in secrets.py)
### Usage
1. Clone this repository.
2. Install the required packages using pip install 'library'.
3. Add your IEX Cloud API key to a file named `secrets.py`.
4. Run the `equal-weight-sp500.py` file using python equal-weight-sp500.py command.
5. Enter the value of your portfolio when prompted.
6. The program will output a DataFrame with the recommended trades and export it to an Excel file named recommended_trades.xlsx.

# Quantitative Momentum Strategy

Quantitative momentum trading is a strategy that involves using statistical analysis to identify stocks that are likely to continue their upward trend. This strategy is based on the idea that stocks that have performed well in the past are likely to continue to perform well in the future.

To implement a quantitative momentum trading strategy, traders typically use a combination of technical analysis and fundamental analysis to identify stocks that are showing strong momentum. This involves analyzing factors such as the stock's price and volume trends, earnings growth, and other financial metrics.

Once potential momentum stocks are identified, traders may use a variety of methods to enter and exit positions. One common approach is to use a trend-following strategy, where traders buy stocks that are trending upward and sell stocks that are trending downward. Another approach is to use a mean-reversion strategy, where traders buy stocks that have experienced a short-term pullback but are still showing strong long-term momentum.

Quantitative momentum trading strategies can be implemented using a variety of tools, including algorithmic trading systems and technical analysis software. These tools can help traders to identify potential trades quickly and efficiently, and can help to automate the trading process to reduce the risk of human error.

It's worth noting that quantitative momentum trading can be a high-risk strategy, and traders should be prepared to manage their risk carefully. It's important to maintain a diversified portfolio and to use proper risk management techniques, such as stop-loss orders, to limit losses in case of market downturns.

### Requirements
- Python 3.6 or higher
- numpy 1.20.1 or higher
- pandas 1.2.2 or higher
- requests 2.25.1 or higher
- xlsxwriter 1.3.7 or higher
- statistics
- IEX Cloud API key (saved in secrets.py)
### Usage
To run this script, you will need an IEX Cloud API key. You can sign up for a free sandbox account at https://iexcloud.io/. Once you have an API key, create a file named `secrets.py` in the root directory of this project and define a variable called `IEX_CLOUD_API_TOKEN` with your API key as its value.

```arduino
IEX_CLOUD_API_TOKEN = 'your-api-key'
```
Next, execute the following command to run the script:
```
python quantitive-moment.py
```
The script will prompt you to enter the value of your portfolio. Once you have entered a value, the script will generate an Excel file named `momentum_strategy.xlsx` in the root directory of this project. This file will contain a list of 50 stocks that have the highest momentum score, along with the number of shares to buy for each stock based on the value of your portfolio.

# Quantitative Value Strategy

Quantitative value trading is a strategy that involves using quantitative analysis to identify undervalued stocks that have strong fundamentals. The idea behind this strategy is that stocks that are currently trading below their intrinsic value are likely to appreciate in price over time.

To implement a quantitative value trading strategy, traders typically use a variety of financial metrics and ratios to identify stocks that are undervalued. This can include analyzing factors such as a company's price-to-earnings ratio, price-to-book ratio, dividend yield, and other fundamental indicators.

Once potential undervalued stocks are identified, traders may use a variety of methods to enter and exit positions. One common approach is to use a contrarian strategy, where traders buy stocks that are out of favor with the market but are showing strong long-term value potential. Another approach is to use a mean-reversion strategy, where traders buy stocks that have experienced a short-term pullback but are still showing strong long-term value potential.

Quantitative value trading strategies can be implemented using a variety of tools, including algorithmic trading systems and financial analysis software. These tools can help traders to identify potential trades quickly and efficiently, and can help to automate the trading process to reduce the risk of human error.

It's worth noting that quantitative value trading can be a high-risk strategy, and traders should be prepared to manage their risk carefully. It's important to maintain a diversified portfolio and to use proper risk management techniques, such as stop-loss orders, to limit losses in case of market downturns. Additionally, traders should be prepared to conduct ongoing analysis and monitoring of their positions to ensure that their trades remain aligned with their investment objectives.

### Trading Strategy Backtesting Project
This repository contains Python code that implements a quantitative trading strategy based on Joel Greenblatt's "Magic Formula Investing" strategy.

The main Python file (quantitive-value.py) uses the IEX Cloud API to retrieve financial data on stocks listed on the S&P 500 index, and then applies a ranking system based on the price-to-earnings ratio and the return-on-capital, as recommended by Greenblatt. The program then selects the top 50 stocks based on this ranking system and calculates the number of shares to buy for each stock, based on the value of the user's inputted portfolio.

In addition, the program calculates various financial ratios such as price-to-earnings ratio, price-to-book ratio, price-to-sales ratio, EV/EBITDA, EV/GP, and percentile rankings for each of these ratios. This information is used to create a "value score" for each stock, which is used to rank the stocks and select the top 10 stocks for investment.

### Requirements
- Python 3.6 or higher
- numpy 1.20.1 or higher
- pandas 1.2.2 or higher
- requests 2.25.1 or higher
- xlsxwriter 1.3.7 or higher
- statistics
 - IEX Cloud API key (saved in secrets.py) 
### Installation
1. Clone the repository to your local machine.
2. Install the required packages by running the following command in your terminal:
```bash
pip install 'library'
```
### Usage
1. Sign up for an account at IEX Cloud.
2. Retrieve your IEX Cloud API token and save it in a separate file called secrets.py in the same directory as magic_formula_backtest.py.
3. Run the program using the following command in your terminal:
```bash
python quantitive-value.py
```
4. Enter the value of your portfolio when prompted.
5. The program will output the top 10 recommended stocks to buy based on the Magic Formula Investing strategy.
