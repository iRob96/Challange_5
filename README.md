# Challange_5

Financial_planning

This app lets users visualize their current savings and determine if they have enough for an emergency fund.
It also forecasts performance of their portfolio showing them where they should be in 30 & 10 years.

---

## Tech Used

Python 3.7
Jupyter Lab
Alpaca API (Application Programming Interface)
Alpaca SDK (Software Development Kit)
MCForecastTools

---
## Install Guide

Install libraries in python by going to the terminal and typing the following:
Requests- conda install -c anaconda requests
JSON- conda install -c jmcmurray json
dotenv- pip install python-dotenv
Alpaca SDK- pip install alpaca-trade-api

--
Alpaca APIs

You have to go to Alpaca markets sign-ip page and create an account to get an API key & secret key to be able to pull from the site.

##Use

We were given a value for monthly income we had to set that as a variable. Then we had to set URL variables for BTC and ETH. That is done by putting "" around the website link. We then pulled info from the URLS using the JSON function. From there we pulled the price of each cryptocurrency then we multiplied it by the amount we had of each which was given to use to calculate the value.

After that we used the API call to pull values for our stocks, AGG & SPY. We used the isoformat function to pull values from a specific day. We used those values and multiplied them with the amounts of each stock we had which was given.

We calculated our total value by adding them all together. We took that value and made sure it was 3x our monthly income to ensure we had an emergency fund.

We used those same values and made a Monte Carlo simulation using those total stocks/bonds value and the MC simulator. We use the formula MCSimulation( portfolio_data = closing_prices_df, weights = [stock 1 weight,stock 2 weight],num_simulation= how many simulations you want, num_trading_days= 252*number of years)

That simulates the values for how ever many years you'd like. We used the values generated to plot and forecast what the client would have in a 30year span and a 10year span.

