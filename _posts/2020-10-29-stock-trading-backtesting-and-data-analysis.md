---
date: 2020-10-29T23:48:05.000Z
layout: post
title: Stock-Trading Backtesting and Data Analysis
subtitle: Develop profitable asset allocation portforlio better than traditional All-weather portfolio
description: >-
  In this project, we developed the asset allocation portforlio in order to secure stable funds after retirement. This project based on Data Mining and Economic statistics.
image: >-
  https://user-images.githubusercontent.com/68367134/97185701-bbc1fe00-17e3-11eb-9d31-46d8ad0e3895.png
optimized_image: >-
  https://user-images.githubusercontent.com/68367134/97185701-bbc1fe00-17e3-11eb-9d31-46d8ad0e3895.png
category: Regression
tags:
  - regression
  - finance
author: 이태헌, 김희주
paginate: true
---
# Stock-Trading Backtesting and Data Analysis

### Develop profitable asset allocation portforlio better than traditional All-weather portfolio

In this project, we developed the asset allocation portforlio in order to secure stable funds after retirement. This project based on Data Mining and Economic statistics.

team: 이태헌, 김희주

### Backtesting
* We downloaded stock trading data and extract close data. Then we analyzed correlation between 5 indexes and profitability & volatility.

#### Steps for backtesting 
* Define strategy
* Back Test using historical data
* Result Analysis
* Develop portfolio based on analysis
* Compare profitability,volatility prediction


### Data Sources : [Investing.com](https://www.investing.com/)
Index 

    Index: SP_Index, Interm_Index, Longterm_Index, Commodity_Index, Gold_Index
    feature : weekly data
    period: 1996.07.01 ~ 2020.06.29(25 years)
    
ETF    

    ETF: SPY, IEF, TLT, DBC, GLD
    feature: weakly data
    period: 2006.06.26 ~ 2020.06.29(15 years)
    
### Define a Problem
* High Relative Poverty Rate for the Elderly in Korea
![1](https://user-images.githubusercontent.com/68367134/97185204-20308d80-17e3-11eb-80ba-af56ae278924.png)


## Data Processing

* comparison about rate of cumulative return by asset types
![Screen Shot 2020-10-26 at 23 34 28](https://user-images.githubusercontent.com/68367134/97185701-bbc1fe00-17e3-11eb-9d31-46d8ad0e3895.png)


### Portfolio
- portfolio_1 : stock 100%
- portfolio_2 : stock 60% + long-term bond 40%
- portfolio_3 : All_Weather : stock 30% + long-term bond 40% + mid-term bond 15% + commidity 7.5% + gold 7.5%
![Screen Shot 2020-10-26 at 23 36 33](https://user-images.githubusercontent.com/68367134/97185929-06dc1100-17e4-11eb-95c9-7f75cdcb5d45.png)



### Trend Analysis about Rate of Cumulative Return by the Portfolios
* Backtest Result for the Traditional All-weather
- All_weather portfolio doesn't seem to be the best portfolio in terms of investment, since the rate of cumulative return is 170% over the last 25 years even though it's safer than any others. 
- Therefore, we think that it would be valuable to build a new portfolio that is able to make more returns as maintaining the safeness of All_Weather portfolio.
![Screen Shot 2020-10-26 at 23 38 41](https://user-images.githubusercontent.com/68367134/97186200-57536e80-17e4-11eb-955e-f9ee4a33291c.png)
![Screen Shot 2020-10-26 at 23 38 47](https://user-images.githubusercontent.com/68367134/97186205-58849b80-17e4-11eb-9c49-d2c82c3f3c60.png)
    
### New Portfolio
- increasing the weight of the assets which are more correlated with SP_500(stock) 

* Correlation Matrix 
![Screen Shot 2020-10-26 at 23 44 02](https://user-images.githubusercontent.com/68367134/97187148-84545100-17e5-11eb-8992-461f91ff97bf.png)

* New Portfolio's Composition
![Screen Shot 2020-10-26 at 23 44 19](https://user-images.githubusercontent.com/68367134/97187167-89190500-17e5-11eb-88e9-afc4ef46af18.png)

### Trend Analysis about Rate of Cumulative Return by New Portfolios
* Backtest Result for All-weather portfolio 4
- All-weather portfolio 4(stock 50%, long_bond 20%, mid_bond 5%, commodity 5%, gold 20%) records the highest cumulative returns with decreased numbers of negative returns
![Screen Shot 2020-10-26 at 23 44 32](https://user-images.githubusercontent.com/68367134/97187181-8cac8c00-17e5-11eb-9a67-ab45fe01427e.png)
![Screen Shot 2020-10-26 at 23 44 43](https://user-images.githubusercontent.com/68367134/97187192-90401300-17e5-11eb-8eb9-6433454d02e3.png)

## Retirement Fund
- To launch a service with the All-weather portfolio 4
- The fund consists of the sum of ETF assets' price after dividing by 500.
- Prices are based on ratio of the All-weather portfolio 4.
![Screen Shot 2020-10-26 at 23 59 50](https://user-images.githubusercontent.com/68367134/97188822-4821f000-17e7-11eb-91fa-51fb6c55f947.png)

### EXPECTED RATE OF RETURN AND RISKS OF RETIREMENT FUND
#### Perfomance Metrics
- Yearly Average Log Rate of Return
![Screen Shot 2020-10-27 at 0 16 34](https://user-images.githubusercontent.com/68367134/97190889-a059f180-17e9-11eb-92df-f7e809185df1.png)

- Yearly Average Log Rate of Return for All-weather Portfolio 4
![Screen Shot 2020-10-27 at 0 03 17](https://user-images.githubusercontent.com/68367134/97189266-bd8dc080-17e7-11eb-82c9-f8faceeaf98a.png)

#### Risk(Volatility)
1. Standard Deviation
- calcualtion of standard deviation to see the possibility if the portfolio can achieve expected rate of return

![Screen Shot 2020-10-27 at 0 06 48](https://user-images.githubusercontent.com/68367134/97189762-4ad11500-17e8-11eb-84f8-a583da68c2a7.png)


2. Sharpe Ratio
- ('return of portfolio' - 'risk-free rate') / (standard deviation of the portfolio’s excess return)
- assumed 'risk-free rate' as 1% interest of Kakao bank saving

![Screen Shot 2020-10-27 at 0 06 55](https://user-images.githubusercontent.com/68367134/97189772-4c9ad880-17e8-11eb-8a2f-3387957e53ef.png)

## Conclusion
- It is found that All-weather portfolio 4 is the best 'assest allocation portfolio' to increase returns with the limited risk of loosing investment. 

### What would the expected return if a person who start to invest our retirement fund from 30-year old to 59-year old? 
- Assumption
    1. buying once a year by price on last week of every June
    2. setting up the exchange ratio as 1,100 won to 1 dollar
    3. 4,000,000 wons - 3,637 dollars
    4. impossible to buy more funds over 4,000,000 wons, and ignore the rest of investment money
    5. ignore dividend of ETF

![Screen Shot 2020-10-27 at 0 08 47](https://user-images.githubusercontent.com/68367134/97189958-866bdf00-17e8-11eb-8ecd-df0ad0eaf3ff.png)
