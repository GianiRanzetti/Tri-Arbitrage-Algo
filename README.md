# Cryptocurrency Tri-Arbitrage Trading Algorithm
## General
This project contains a Python trading model that determines risk-free arbitrage strategies between three crypto coin-pairs. The strategy relies on finding arbitrage "triangles". When converting a cryptocurrency through each of the 3 pairs and back to the original cryptocurrency, the law of one price states that executing the transaction "clockwise" or "anti-clockwise" through the triangle returns the same amount. If not, there exists an anomaly in the exchange rates that can be profited from. This algorithm identifies arbitrage opportunities in the market due to mispricings and returns trade signals.

## Getting Started
### Install the CCXT library:
```
!pip install ccxt
```
### Import Kraken and Pandas:
```
import ccxt
import pandas as pd
```
### Execute the 3 Project Code Files:

File 1: "Obtaining Sample Data" - Connects to the Kraken API and retrieves real-time data for 3 coin-pairs. These are limited by the availability of the Kraken database. The code retrieves the 3 highest bids and ask orders for each pair and the last traded price.

File 2: "Trading Algorithm" - Contains all the logic of the trading strategy. The algorithm calculates discrepancies in pricing by comparing returns from currency conversion "clockwise" or "anti-clockwise" through the triangle. If an opportunity is found, the model will return a buy or sell signal, the relevant crypto pair to be traded, and an order amount. The code will also take into account the exchange's fees and the bid-ask spread. Furthermore, a one-time transaction is included to simulate a large position in a chosen crypto.

File 3: "Algorithm Execution" - Creates an Order Book containing all transactions given by the trading algorithm. In this project version, the orderbook is stored locally. Furthermore, a profit and loss measure is updated after each transaction. The Order Book is stored locally.

## Limitations
The last file of the project, "Algorithm Execution" only executes the trades within the confines of the script. An improvement that could be made is to connect the orderbook with a crypto exchange to execute the trades in real time. It would be difficult to implement because the code is quite slow (it takes a couple seconds to execute) compared to the milliseconds required to successfully capitalize on arbitrage opportunities.
