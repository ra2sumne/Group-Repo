Project 1: 
Team 1:

__Contributors:__ 
- Rawlric Sumner
- Rasha Mosaad
- Emmanuel Henao
- Takeshi Nagai
- Michael De Paula
- Priya Roy


<p align="center">
    <ins><b>Growth of Mining Stocks: “Where do I invest my money?”</b><br><ins>
    
</p>

### __Core message or hypothesis for your project:__ 
With the economic slowdown due to the pandemic, the mining industry is at the forefront of other strategic industries that are well positioned for growth. Our team became interested in creating an online interactive one-stop tool for investors where they can follow the changes in the Mining Industry and the impact of supply and demand of energy nation-wide on the growth of mining stocks. With this tool, Investors are also able to select certain stocks for investment based on a quick view of industry-specific valuation metrics and charts. 


Describe the questions you and your group found interesting and what motivated you to answer them.
The team was interested in the following:
- Finding if the gap between total US production of energy and total consumption of energy is driving the mining stocks growth. Towards that end, we looked for:	
Data of total consumption and production by state on an annual basis,
Data for geographical locations of mines by state,
Data on longitude and latitude by state to create the U.S. map with the mine locations,
Creating a dashboard for investors who are interested in Mining stocks to provide investors with a quick update on the industry and to help them make investment decisions based on certain financial metrics. 
- Our initial plan was to provide financial analysis based on real-time data, but it turned out to be infeasible for the scope of this project since most databases we were trying to tap into charged top dollar membership fees. Due to this limitation, we decided to use static financial data as opposed to dynamic financial data.


### __Data used for project:__ 

- __[Energy Information Administration](https://www.eia.gov/)__
- __[Yahoo! Finance](https://finance.yahoo.com/)__
- __[PWC](https://www.pwc.com/gx/en/research-insights.html0)__
- __[U.S. Geological Survey](https://www.usgs.gov/)__ 

### __Describe the data exploration and cleanup process (accompanied by your Jupyter Notebook).__
 We created five jupyter notebook files in order to seperate the code for requirements of our data. Within each notebook we started by either pulling data from a CSV from a database listed above or an API like Alpaca. We then parsed through the data and cleaned it using usecols, header and nrows. 
 
 We also imported the following  libraries:
 - import os
 - import re
 - import pandas as pd
 - import numpy as np
 - from dotenv import load_dotenv
 - from pathlib import Path
 - import panel as pn
 - pn.extension("plotly") 
 - from panel.interact import interact
 - import hvplot.pandas
 - import plotly.express as px
 - import plotly.graph_objects as go
 - import base64
 - import dash
 - import dash_core_components as dcc
 - import dash_html_components as html
 - import dash_bootstrap_components as dbc
 - from dash.dependencies import Input, Output
 - %matplotlib inline 

### __Describe the analysis process (accompanied by your Jupyter Notebook).__

The analysis code is contained in the following jupyter files:
- [Stock Analysis Code](https://github.com/ra2sumne/Group-Repo/blob/main/Stock_data_financial_analysis.ipynb)
- [Energy and Production Analysis](https://github.com/ra2sumne/Group-Repo/blob/main/Energy_prod_con_analysis.ipynb)
- [Monte Carlo Simulations](https://github.com/ra2sumne/Group-Repo/blob/main/Stock_data_monte_carlo.ipynb)

Our initial goal was to provide real-time financial analysis for mining stocks to help investors make decisions on which of the top mining industry stock to invest in. We selected the top mining stocks based on market capitalization. 

All ten stocks:	
- Have a minimum market cap of $1 Billion for each.
- U.S. based (domestic as opposed to foreign). 
- Listed on NYSE with same reporting requirements and similar financial statements.
- Global top performing mining companies list for 2020.

As we started looking into different free sources of financial data, we found that most APIs are providing free real-time downloadable data only for stock price quotes, daily traded shares volume and closing prices. For the purposes of our project, we needed more in-depth data to conduct our financial analysis. After spending some time researching available API’s and databases, we decided to use __[Yahoo! Finance](https://finance.yahoo.com/)__ to pull the financial data we needed, therefore, we decided to use static data to perform as accurate of a financial analysis possible.

Summarize your conclusions. This should include a numerical summary (i.e., what data did your analysis yield), as well as visualizations of that summary (plots of the final analysis data).

Our hypothesis is that the gap between production and consumption is driving growth in mining stocks. However, data showed that the gap between supply and demand has been declining and in 2019, for the first time, production exceeded consumption.



We reflected our findings to show the production exceeding consumption in 2019 using an ‘hvPlot’ bar graph. U.S. energy consumption will continue to grow more slowly than gross domestic product as U.S. energy efficiency continues to increase. 

We also created an interactive plot with a dropdown menu for all the stocks and fixed the industry benchmark as ‘XME’ to enable investors at comparing the performance of each stock to the performance of the industry benchmark over the period of five years. 

Based on these findings we then started thinking that global energy might be driving growth in mining stocks, however for the time scope of our project we were not able to pursue this further. Initially, we tried to draw a correlation between global demand changes and mining stock prices for the stocks selected, however, this was deemed inconclusive as more time is needed to test the theory.  

Going into the financial analysis we decided to focus on certain financial valuation metrics pertaining to the Mining industry.
- Standard Deviation
- Daily Returns
- Sharpe Ratios
- Correlations
- Monte Carlo Simulations

 We then created a plot for stocks to show the top performer according to each metric. For the scope of this project we limited them down to P/E ratio to pick the cheapest stock out of them, Dividend Yield and Dividend Rate for investors who are looking for dividend paying stocks especially pensioners and retirement funds, Average Rate of Returns over five years (2015-2019) for each stock, Volatility (standard deviation), and the Sharpe ratio for investors who would like to know how much each unit of investment risk is worth. 


### __Best Performers:__
### __CLF__
For the five years from 2015 to 2019, CLF generated the highest average rate of return, which would be top pick for investors who are looking for steady growth of income.

### __NUE__
Based on the Trailing Annual Dividend Yield metric, NUE was the stock with the highest value, which makes it a good stock choice for pensioners and retirement funds that have a buy and hold strategy while generating a steady income from dividends on the side.


#### Volatility: 
We looked at the volatility of the stocks in two ways: 	First we wanted to rank the stocks in terms of volatility so we created an hvplot boxplot. We then used this chart in conjunction with the Sharpe ratios for the stocks to help investors identify which stocks are worth the risk (high volatility) relative to the others depending on the investor's risk appetite. The companies with the higher risks were CLF, FCX and HL. 

The last step was to find the correlation between the XME, which is the mining industry index benchmark, and the stocks we picked. We used XME vs. other indices as it tracks an equally-weighted index of U.S. metals and mining companies and would be a good indicator for the performance of mining and metals markets. We used a heat-map to show the correlation between the stocks and the industry benchmark.

### __Conclusion:__
Ultimately, if time were not an issue our goal would be to not limit the amount of stocks that can be used to make a decision as well as not limit the application to an industry sector but make it available to all sectors of the market. We would have liked to make this a complete market ready application by including additional interactions for the user for example selecting their investor profile or time horizon to help make an even better decision ont he stocks selected. 


_______________________________________________________________
_______________________________________________________________


<p align="center">
    <ins><b>Below are a list and brief description of stocks selected:</b><br><ins>
    
</p> 

__FCX:__

Freeport-McMoRan (FCX) is a leading international mining company with headquarters in Phoenix, Arizona established on November 10, 1987. They operate large, long-lived geographically diverse assets with significant proven and probable reserves of copper, gold and molybdenum. Their portfolio of assets includes the Grasberg minerals district in Indonesia, one of the world’s largest copper and gold deposits; and significant mining operations in the Americas, including the large-scale Morenci minerals district in North America and the Cerro Verde operation in South America.
FCX is a founding member of the International Council on Mining and Metals (ICMM). Implementation of the ICMM Sustainable Development Framework across the company results in site-level sustainability programs that meet responsible sourcing objectives for the global marketplace.
 
__NUE:__

Nucor Corporation is a producer of steel and related products headquartered in Charlotte, North Carolina. It is the largest steel producer in the United States, and is the largest "mini-mill" steelmaker (i.e. it uses electric arc furnaces to melt scrap steel as opposed to blast furnaces to melt iron) and is the largest scrap recycler in North America. In 2019, the company produced and sold approximately 18.6 million tons of steel and recycled 17.8 million tons of scrap. Nucor operates 23 scrap-based steel production mills.[1]
Nucor produces steel bars (carbon and alloy steel), beams, sheet / flat rolled steel, plate, steel joists, joist girders, steel deck, fabricated concrete reinforcing steel, cold finished steel, steel fasteners, metal building systems, light gauge steel framing, steel grating, expanded metal, and wire mesh. In addition, through Companies being for projects:hits David J. Joseph Company subsidiary, Nucor also brokers ferrous and nonferrous metals, pig iron and HRI/DRI; supplies ferro-alloys; and processes ferrous and nonferrous scrap.
 
 
 
__STLD:__

Steel Dynamics, Inc., is a steel producer based in Fort Wayne, Indiana with a production capacity of 13 million tons, Steel Dynamics is the 3rd largest producer of carbon steel products in the United States. SDI is among the most profitable American steel companies in terms of profit margins and operating profit per ton. Steel Dynamics was founded in 1993 by three former executives of Nucor with $370 million in funding. It began production at its $275 million Butler, Indiana, flat roll mill in 1996 and reported its first annual profit in 1997.
 
__AA:__

Alcoa Corporation (Aluminum Company of America) is the world's eighth largest producer of aluminum,[2] with corporate headquarters in Pittsburgh, Pennsylvania.[3] Alcoa conducts operations in 10 countries. Alcoa is a major producer of primary aluminum, fabricated aluminum, and alumina combined, through its active and growing participation in all major aspects of the industry: technology, mining, refining, smelting, fabricating, and recycling. Alcoa has ownership in seven active bauxite mines globally and operates four of them, making us among the largest bauxite producers in the world. We have access to large bauxite deposits with mining rights that extend in most cases more than 20 years. Our global network is strategically located near key Atlantic and Pacific markets. It includes the Huntly mine in Australia, the second largest bauxite mine in the world.
Alcoa offers bauxite from its mines to meet customer-specific needs and provide a consistent, reliable, and sustainable supply of raw material for refineries around the globe.
We are the world's leading producer of alumina. With installed refinery capacity of 17 million metric tons per year, we currently operate six refineries in Australia, Brazil and Spain, and have a 25 percent share in the refinery that is part of our Ma’aden joint venture in Saudi Arabia. Our three-refinery operation in Western Australia is the world's biggest single source of alumina, able to supply eight percent of the global market.
Alcoa is a global aluminum supplier and its product portfolio includes Bauxite, Alumina and Aluminum. Our Aluminum segment includes aluminum smelting, casting, and rolling, along with the majority of the energy assets.

__WPM:__

Wheaton Precious Metals is one of the largest precious metals streaming companies in the world. The Company has entered into agreements to purchase all or a portion of the precious metals or cobalt production from high-quality mines for an upfront payment and an additional payment upon delivery of the metal. Wheaton currently has streaming agreements for 20 operating mines and 9 development stage projects. The Company’s production profile is driven by a portfolio of low-cost, long-life assets, including a gold stream on Vale’s Salobo mine, and a silver stream on Newmont's Peñasquito mine. It produces over 26 million ounces and sells over 29 million ounces of silver mined by other companies. Silver Wheaton was established in 2004. It was previously controlled by Goldcorp until December 7, 2006 when Goldcorp's sale of 18 million shares reduced its ownership to 48%. 

__ALB:__

Albemarle Corporation is a fine chemical manufacturing company based in Charlotte, North Carolina. It operates 3 divisions: Lithium, Bromine and Catalyst solutions. We think beyond business-as-usual to power the potential of companies in many of the world's largest and most critical industries, such as energy, electronics, and transportation. We actively pursue a sustainable approach to managing our diverse global footprint of world-class resources. In conjunction with our highly experienced and talented global teams, our deep-seated values, and our collaborative customer relationships, we create value-added and performance-based solutions that enable a safer and more sustainable future.

__NEM:__

Newmont is the world’s leading gold company and a producer of copper, silver, zinc and lead. The Company’s world-class portfolio of assets, prospects and talent is anchored in favorable mining jurisdictions in North America, South America, Australia and Africa. Newmont is the only gold producer listed in the S&P 500 Index and is widely recognized for its principled environmental, social and governance practices. The Company is an industry leader in value creation, supported by robust safety standards, superior execution and technical proficiency. Newmont was founded in 1921 and has been publicly traded since 1925. Newmont's mission is to build a sustainable mining business while leading in safety, environmental stewardship and social responsibility. Today, we primarily mine gold and copper, as well as silver and other metals and minerals.
 
__HL:__

A silver and gold producer with assets in the U.S., Canada and Mexico founded in 1891 and is the largest primary producer of silver in the U.S. and the fifth largest gold producer in Quebec. By the end of 2020, Hecla expects to generate 10.9 million-11.9 million oz. silver and 195,000-208,000 oz. gold.
Hecla’s wholly owned Greens Creek underground mine in southeast Alaska is, according to the company, one of the largest and lowest-cost primary silver mines in the world. Last year, Greens Creek churned out 9.9 million oz. silver and 56,625 oz. gold at cash costs of US$1.97 per oz. silver, after by-product credits.
In western Quebec, Hecla’s wholly owned Casa Berardi underground gold mine produced 134,409 oz. gold last year at cash costs (after by-product credits) of US$1,051 per oz. and was acquired back in 2013 through its acquisition of Aurizon Mines.
In 2018, the company acquired Klondex Mines in a US$462-million cash-and-share deal, which added the Fire Creek, Hollister and Midas gold and silver mines in Nevada to its asset portfolio.
In Idaho, Hecla holds the Lucky Friday underground operation, within the state’s Coeur d’Alene mining district. The mine has been producing silver since 1942 and, according to the company, still has 20 to 30 years of mine life ahead.
Hecla’s Mexican asset is the San Sebastian silver and gold mine, which started up in 2015 and covers 420 sq. km within the Mexican Silver Belt.
The company’s pre-production assets include the Montanore silver-copper deposit in Montana as well as the Rock Creek property, 80 km north of the Lucky Friday mine. Hecla also holds exploration properties in Colorado, Idaho and Nevada as well as B.C. and Quebec.

__CLF:__

Founded in 1847, Cleveland-Cliffs is among the largest vertically integrated producers of value-added iron ore and steel products in North America. In March 2020, the Company completed the acquisition of AK Steel. With the acquisition of AK Steel, Cleveland-Cliffs now holds an industry-leading market position in automotive steel, where its portfolio of high-end products delivers a broad range of differentiated solutions for this highly sought after customer base. Cleveland-Cliffs will also be the sole producer of hot briquetted iron (HBI) in the Great Lakes region when its first plant starts up in mid-2020. Collectively, Cleveland-Cliffs and AK Steel have an extensive history of being innovators dating back more than a century. From upstream research and development, to downstream applications, the Company has dedicated technical and engineering resources that begin with improving customers’ production and manufacturing performance to applications for their end product use. Built on a strong legacy of safety and environmental stewardship, Cleveland-Cliffs mines responsibly and produces environmentally friendly iron ore pellets that enable production of clean steelmaking. The Company produces steel, the most recycled material on the planet. From a focus on key environmental processes such as steel recycling and water reuse, to corporate and social responsibility, sustainability is core to the company’s values and operations.
Cleveland-Cliffs is the largest and oldest independent iron ore mining company in the U.S. Widely recognized for innovation in iron ore mining and processing technologies, Cleveland-Cliffs is a major supplier of iron ore pellets from its mines and pellet plants in Michigan and Minnesota. Cliffs produces various grades of pellets, including standard, fluxed and DR-grade, for North American steel customers.
