# Cryptocurrency Tri-Arbitrage Trading algorithm
## General
A python trading model that determines risk-free arbitrage strategies between 3 coin-pairs and executes trades when detected.
This algorithm retrieves real-time data from the Kraken library and executes the trades locally.

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

File 1: "Obtaining Sample Data" - Connects to the Kraken API and retieves real time data for 3 coin-pairs. These are limited by the availability of the Kraken database. The code retrieves the 3 highest bid and ask orders for each pair and the last traded price.

File 2: "Trading Algorithm" - Connects to the Kraken API and retieves real time data for 3 coin-pairs. These are limited by the availability of the Kraken database. The code retrieves the 3 highest bid and ask orders for each pair and the last traded price.

File 3: "Algorithm Execution" - Connects to the Kraken API and retieves real time data for 3 coin-pairs. These are limited by the availability of the Kraken database. The code retrieves the 3 highest bid and ask orders for each pair and the last traded price.
