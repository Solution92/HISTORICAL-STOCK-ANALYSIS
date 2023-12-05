# HISTORICAL-STOCK-ANALYSIS
This is the Analysis of the prices of 10 popular companies (Apple, Amazon, Netflix, Microsoft, Google, Facebook, Tesla, Walmart, Uber, and Zoom), within the period of seven years — 2015–2021.

## Table of Content
- [Project Objective](#project-objective)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis](#data-analysis)
- [The Dashboard](#the-dashboard)
- [Result and Findings](#result-and-findings)
- [Recommendation](#recommendation)
- [Limitations](#limitations)
- [Reference](#reference)


### Project Objective

The following may form the purpose of this Analysis, to do Exploratory Data Analysis with a clear Visualization tool to compare the stock price growth between companies to predict stock prices.

### Data Source

The dataset was provided in a CSV file format by the client which I am not permitted to disclose.

### Tools Used

- MS Excel (INDEX MATCH) - Merging and Consolidation
- Power BI — Data Cleaning, Transformation, Analysis, and Creating Reports.

### Data Cleaning and Preparation

The Datasets. Understanding the ETL Process is as important as understanding the Dataset itself and this is a major part of the foundation of analysing the data. The Dataset was presented differently in a Text/CSV format. This means that I had ten (10) CSV files representing the different Companies.

Each of these files has seven(7) different Columns — “Date”, “Open”, “High”, “Low”, “Close”, “Adjusted Close”, and “Volume”, with over 1,000 rows. The “Date” here, is the trading date the transactions took place, and the “Open” represents the opening price of the stock. The “High”, is the highest price of a stock for that day while the “Low” is the opposite, the lowest price of the stock for that day’s transaction.
The “ Close” is the closing price for the day while the “Adjusted Close” is the stock’s closing price that has been amended to include any distribution/corporate actions that occur before the next day’s “open”.

After Data has been extracted from various sources such as databases, files, or APIs. Extraction involves identifying and retrieving the relevant data for analysis. The next process is the Transformation process to make it suitable for analysis.

Transformations can include cleaning, filtering, merging, and reformatting the data. This step is crucial for ensuring data quality and consistency.

The first thing I did was to Consolidate these different files into one Table in Excel using INDEX MATCH functions for easy accessibility and understanding.

![Screenshot_128](https://github.com/Solution92/HISTORICAL-STOCK-ANALYSIS/assets/144762124/71efb65a-4249-4376-ac4c-d412d86c5754)
Consolidated Table

I further loaded it to the Power query editor where I cleaned up the “null” values, and Errors created the “Year” and “Month” Columns respectively. It may interest you to know that after the cleaning and transformation, the Dataset now has 124 Columns.

### Exploratory Data Analysis (EDA)

Report and Visualization, after data is extracted and transformed, it is loaded into a target data repository, typically a data warehouse or database, where it can be accessed by analysts and tools for reporting, visualization, or further analysis.

In this step, I created different APIs as well as the visuals.

Key Performance Indicators (KPIs)

- Totaltraded Volume
- AVG Traded Volume
- Total Open
- Total Close

ANALYSIS/INSIGHTS

- Yearly Traded Volume by Company
- Sum of High Price by Year
- Sum of Open Price by Year
- Sum of Close Price by Month
- Sum of Low Price by Year
- Monthly Traded Volume

### Data Analysis
~~~
- Totaltraded Volume = Total Traded Volume = SUM(HistoricalStock[ Total_Traded_Volume ])

- AVG Traded Volume = AVERAGE(HistoricalStock[ AVG_Traded_Volume ])

- Total Open = SUM(HistoricalStock[ Total_Open ])

- Total Close = SUM(HistoricalStock[ Sum_Close ]) + SUM(HistoricalStock[ Sum_Close2 ]) + SUM(HistoricalStock[ Sum_Close3 ]) + SUM(HistoricalStock[ Sum_Close4 ]) + SUM(HistoricalStock[ Sum_Close5 ]) + SUM(HistoricalStock[ Sum_Open6 ]) + SUM(HistoricalStock[ Sum_Close7 ]) + SUM(‘HistoricalStock’[ Sum_Close8 ]) + SUM(HistoricalStock[ Sum_Close9 ]) + SUM(HistoricalStock[ Sum_Close10 ])
~~~

### The Dashboard

![Screenshot_129](https://github.com/Solution92/HISTORICAL-STOCK-ANALYSIS/assets/144762124/396c0cc0-2f06-4342-a1b7-0122e5d145c2)

### Result and Findings

Below are my findings from the Historical Stock Analysis

= At 1,071,901,800, 2020 had the highest Sum of Amazon Volume and was 82.45% higher than 2019, which had the lowest Sum of Amazon Volume at 587,492,500.  2020 accounted for 41.53% of the Sum of Amazon Volume.  2019 had 587,492,500 Sum of Amazon Volume, 35,134,601,200 Sum of Apple Volume, and 335,190,018 Sum of Google Volume. 2020 had 1,071,901,800 Sum of Amazon Volume, 43,489,431,600 Sum of Apple Volume, and 507402200 Sum of Google Volume. 2021 had 921,390,700 Sum of Amazon Volume, 29,727,787,200 Sum of Apple Volume, and 391,502,900 Sum of Google Volume.  

- Meanwhile, at 32,754.81, 2021 had the highest Sum of Facebook Open and was 120.28% higher than 2019, which had the lowest Sum of Facebook Open at 14,869.46.  The sum of Facebook Open and the total Sum of Google Open are positively correlated with each other.  2021 accounted for 43.33% of the Sum of Facebook Open.  2019 had 14,869.46 Sum of Facebook Open, 99,625.91 Sum of Facebook Open, and 7,959.46 Sum of Microsoft Open. 2020 had 27,961.49 Sum of Facebook Open, 182,584.40 Sum of Google Open, and 13,351.28 Sum of Microsoft Open. 2021 had 32,754.81 Sum of Facebook Open, 199,923.20 Sum of Google Open, and 15,333.66 Sum of Microsoft Open.  

- More so, at 204,411.92, 2021 had the highest Sum of AMZ Low and was 175.72% higher than 2019, which had the lowest Sum of AMZ Low at 74,138.36.  The sum of AMZ Low and the total Sum of FB Low are positively correlated with each other.  2021 accounted for 46.34% of the Sum of AMZ Low.  2019 had 74,138.36 Sum of AMZ Low, 14,708.03 Sum of FB Low, and 5,397.69 Sum of App Low. 2020 had 162,589.39 Sum of AMZ Low, 27,655.84 Sum of FB Low, and 6,570.52 Sum of Apple Low. 2021 had 204,411.92 Sum of AMZ Low, 32,502.69 Sum of FB Low, and 7,796.58 Sum of Apple Low.  

- Additionally, at 207,429.87, 2021 had the highest Sum of AMZ High and was 174.03% higher than 2019, which had the lowest Sum of AMZ High at 75,695.13. The sum of AMZ High and the total Sum of Apple High are positively correlated with each other.  2021 accounted for 46.19% of the Sum of AMZ High. 2019 had 75,695.13 Sum of AMZ High, 5506 Sum of Apple High, and 15,025.66 Sum of FB High. 2020 had 166,000.28 Sum of AMZ High, 6,690.84 Sum of Apple High, and 28,229.25 Sum of FB High. 2021 had 207,429.87 Sum of AMZ High, 7,899.29 Sum of App High, and 32,985.94 Sum of FB High.  

- In the same vein, at 1,734,001,700, February had the highest Sum of FB Volume and was 104.23% higher than December, which had the lowest Sum of FB Volume at 849,032,500. The sum of FB Volume and the total Sum of App_Volume are positively correlated with each other. February accounted for 10.80% of the Sum of FB Volume.  Across all 12 War Months, the Sum of FB Volume ranged from 849,032,500 to 1,734,001,700, the Sum of App_Volume ranged from 5,888,782,400 to 12,560,933,600, and the Sum of Gg_Volume ranged from 75,197,600 to 129,989,422.  

- At 17,585.44, October had the highest Sum of Zoom Close and was 104.56% higher than January, which had the lowest Sum of Zoom Close at 8,596.89.  October accounted for 11.16% of the Sum of Zoom Close.  Across all 12 Uber Months, the Sum of Zoom Close ranged from 8,596.89 to 17,585.44.  

### Recommendation

- Based on the historical stock analysis, it is evident that 2020 was a significant year with the highest Sum of Amazon Volume, indicating a substantial increase compared to 2019. 
- Additionally, 2021 demonstrated notable highs in Facebook Open, AMZ Low, and AMZ High. 
- Positive correlations were observed between certain stock metrics, such as Sum of Facebook Open and total Sum of Google Open. These findings suggest potential investment opportunities in technology stocks, particularly focusing on the highlighted years and associated metrics. 
- Further exploration of the positively correlated stock indicators could aid in forming a diversified and informed investment strategy for maximizing returns.

### Limitations

- The limitations of the table include a lack of detailed context or specific financial metrics, such as stock prices or market indices, which could provide a more comprehensive understanding of stock performance. 
- The absence of information on external factors, market trends, or economic conditions hinders a nuanced analysis of the stock data. 
- Additionally, the table doesn't provide insights into causality, making it challenging to identify the specific reasons behind the observed correlations or trends. 
- It would be beneficial to include more variables and contextual information for a more robust and actionable analysis in the stock market.

### Reference

[kaggle](www.kaggle.com) holds a global database of this nature. 
















