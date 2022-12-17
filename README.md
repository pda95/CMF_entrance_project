### Dataset Description:
This dataset is an augmented Chinese stock market dataset that includes not only OHLC prices and volume data, but also some other financial ratios at daily frequency, like PE, PB, PS ratio, dividend yield, and etc. The covered period is from Jan 4th, 2005, to May 11th, 2022.
All data are available at "daily frequency", including FRs (financial ratios) like PE ratio and some fundamentals like total market cap, etc.
It takes sufficiently large amount of time to gather information/data about all liquid and publicly traded stocks on Shanghai Stock Exchange and Shenzhen Stock Exchange (a total of 4714 stocks, as identified by their ticker symbols).

** Full description of the dataset: **
https://www.kaggle.com/datasets/franciscofeng/augmented-china-stock-data-with-fundamentals


### Task: 
We should implement an algorithmic strategy on data of Chinese companies 

### Dataset Attributes:
**stock_data.csv**:
The "open", "close", "high" & "low" are adjusted stock prices (keeping the latest stock prices unchanged and adjusting the stock prices back into the past). The adjustment factor is "qfq_factor" in this dataset.
Prices are adjusted for consistency reasons, and mostly used for designing and backtesting quantitative trading strategies of any kind.

date : the date in the format of "yyyy-mm-dd"
ticker : the ticker symbol, or stock code in Chinese stock market
high : the highest price of the trading day
low : the lowest price of the trading day
close : the close price of the trading day
volume : the trading volume of the trading day
outstanding_share : a company's stock currently held by all its shareholders
turnover : a measure of stock liquidity
pe : PE (price to earnings) ratio
pe_ttm : trailing Twelve Months PE ratio: the current share price divided by the last 4 quarterly EPS (earnings per share)
pb : PB ratio (price to book ratio)
ps : PS ratio (price to sales ratio)
ps_ttm : trailing 12 months PS ratio
dv_ratio : Dividend yield ratio (the percentage of a company's share price that it pays out)
dv_ttm : Trailing 12 months Dividend yield ratio
total_mv : Total market capitalization
qfq_factor : the price adjustment factor

**ticker_info.csv**:
Mapping the ticker symbol to the company name (in Chinese character) in case users are interested.
Ticker symbols starting with "sh" are traded on the Shanghai Stock Exchange, and ticker symbols starting with "sz" are traded on the Shenzhen Stock Exchange.
"Company_name" that includes "ST" are those companies experiencing serious financial distress and are very likely to go bankrupt/delisted if the companies' financial condition doesn't improve in 3 years.

ticker : ticker symbol
company_name : company name of the "ticker symbol"
