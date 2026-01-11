# Automated-Stock-Trading
Used AngelOne's SmartAPI python SDK to automate one of the trading strategies comprising of Relative Strength Index(RSI) as a technical indicator along with live candlesticks.
Based on the indicators it performs the following tasks:
1. Places buy/sell orders automatically.
2. Checks holdings of the user
3. Computes Technical Indicators
4. Access to Real-Time stock data using websockets
# Project Directory 
It comprises of the following files:
1. **strategy.py** : The file containing the core code of the strategy
2. **main.py** : The main file for placing orders and checking indicators.
# Brief Strategy Description  
The strategy used was an intraday strategy with the following points: 
1. We have already defined a set of ETFs/Stocks who need to be traded
2. We use the RSI Indicator for placing the buy order
3. If RSI reaches greater than 60 for a stock and there is no active position, we place buy order
4. Our initial stoploss will be the low of 30-min candle which will be trailed every 30 mins to the low of new 30-min candle until the stoploss is breached.
5. If the stoploss is hit or it's the end of the day we close our position.
