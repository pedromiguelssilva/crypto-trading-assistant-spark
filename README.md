%md
##### 1. Motivation?
Cryptocurrency, along with its underlying technology - Blockchain, is clearly the latest disruptive technology in fintech, and one of the hottest topics of the 21st century. While controversial, some say it may revolutionize traditional means of payment and exchange and, recently, it has drawn the attention of developers and data scientists, for applications that range from simply learning how to code to building trading bots to assist their trades. **Well, why not do both?**

##### 2. What is the endgame and where is data being pulled from?
We are interested in exploring both historical quotes and the latest quotes (ideally in a streaming format) for a set of selected coins, and then use them to build a trading assistance bot, that will hopefully advise us to buy or sell (or simply do nothing) each coin.   
It is noteworthy mentioning though, that although there are several API's available in the market for pulling crytocurrency prices and volumes data, most of them are not free or provide very little information for free tiers (which makes sense, given how valuable the information can be for skilled analysts). In any case, we were able to find two sources that fill our demands for data:
1. **Yahoo Finance** - a platform that provides news on the financial world and data regarding stock prices, financial reports and every kind of financial information regarding companies, commodities and, luckily for us, cryptocurrencies as well.
2. **CoinMarketCap** - the gold-standard platform in the cryptocurrency world, providing market data and a whole lot of other information on cryptocurrency, including to other platforms like Yahoo Finance itself.

##### 3. How is data being pulled?
* For a while, Yahoo Finance provided an API for free stock market data, but it was closed in 2017. Fortunately, a python module was built by scrapping Yahoo Finance data, named **yfinance**, providing developers with an alternative. We will use this library to access the last 10 years (of course not all of them have such an extended historic) of daily data for crypto prices and traded volumes.
* CoinMarketData provides an API that only requires a free signing up for an access key, which we are using to get the latest quotes, thus emulating a streaming scenario. The basic tier provides a total 333 daily calls to the API, for a total maximum of 10.000 a month, which means we are only able to make a call roughly every 5 minutes (4 minutes and 19 seconds or 259 seconds, to be more precise), which is not perfect, but is perfectly fine for demonstration purposes.
* A third dataset with metadata regarding each cryptocurrency will also be built using data from both sources.
