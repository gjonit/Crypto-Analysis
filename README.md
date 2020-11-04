# Crypto-Analysis
Selects 3 pairs of crypto currencies, saves their data in a MySql database and finds and analyze Log Returns, Value at Risk and Expected Shortfall

# Disclaimers
You need to manually include the Binace API keys.
The Log Returns are stored for eacg pairs table, while VaR and ES are stored in a sperate table called Analysis_Result.

# Steps
1. I began by creating the database host in AWS RDS. The database is public and available to everyone.
2. Made conncetion with Binance API's and retrieve the data of the three pairs (LTCUSDT, ETHBTC, XRPUSDT)
3. Parsed each pair into Pandas DataFrame.
4. Scraped from each pair the Price and the Volume
5. Calculating the % change which leads to calculate the Log Returns.
6. After that I found the Value at Risk. In order to find you need:
          -Value that you are going to invest
          -Confidence Interval
          -Weights (I created 3 random weights and normalized them in order to be used.)
          -Look back period.
7. CVaR( Expected Shortfall follows and it is a better risk management tool then VaR.
8. Plotted the graph for each min that corespondents to VaR in the `lookback` period.
9. Created the Database and made it accesable within the python code.
10. Created the table for each pair of cryptos with 5 columns each that corespondent to Id(minutes), Price, Volume, Percantage Change, Log Returns.
11. Created the result table that holds the Value at Risk and Expected Shortfall.

The Result Table( Value at Risk and Expected Shortfall)
<img width="961" alt="Screen Shot 2020-11-04 at 5 00 33 PM" src="https://user-images.githubusercontent.com/45251476/98172583-9d34c480-1ebf-11eb-9fd2-29055b6e178d.png">





          
  
       

