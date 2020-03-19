# US Used Car Market Analysis from Truecar.com
Jinpeng Gao
March 17th, 2020

## Key words: 
Web scraping, Python, EDA, Machine learning

## Project overview: 
This project serves as the final project of STA220 taught by Professor James Sharpnack in 2020 Spring at UC Davis. As a Ph.D. candidate from Transportation, Technology and Policy major, I am very interested in predicting people's purchase behaviors in vehicle markets. Truecar.com is one of the largest online used car listing websites that provide extensive used car sale information from all over the United States. 
This project is intended to understand the US used car markets by scraping the vehicle information from Truecar.com and explore questions such as the distribution of number of listings, and the distribution of resell prices.

## Website introduction:
The website mainly contains four categories of information
1) Vehicle resell price provided by the dealer.
2) Vehicle geospatial information: state and city where the car is currently located.
3) Vehicle characteristics: vehicle year, make, model, color, mpg, mileage, fuel type, drive type, style, etc.
4) Vehicle history information: number of reported accidents and previous owners, title and usage type, etc.

## Limitations:
Since there are no available api to use, web scraping and html parsing are used to extract information from Truecar.com. However, the website limit the total number of listings to be presented to users as 9900 cars, even though there are over 1 million listed used cars on the website.

When I tried to get the 9900 cars, I used to default 'Best Match' search term to minimize the potential bias caused by the sampling and presenting procedure by the website. 

One of the important assumptions I make is that I assume the 9900 vehicle listings I scraped from the Truecar.com are randomly sampled from the total population. Therefore, the following analysis can well represent the real distribution and characteristics of whole population.

## Questions:
Some questions I am interested to answer include:
1) What's the geospatial and temporal distribution of number of used cars? How other variables impact the distribution of listings?
2) What's the most popular make and model of used cars? What's the most popular colors, and the most popular features?
3) How will the mpg impact the resell price?
4) How does the vehicle history (number of previous owners, title, usage_type, number of accidents) impact the resell price?
5) Is certified pre-owned cars more expensive than normal used cars?
6) For similar cars, are the prices in CA higher than out of CA?
etc...

## Notebooks:
There are 4 notebooks in the project and each works for one important function in the project, which includes:
1. WebScraping: scrape the webpages and parsing all the vehicle webpages, save the raw data to csv file, 'usedCarListing.csv'.
2. DataMunging and FeatureEngineering: clean the data in terms of missing data, wrong data, get rid of unnessesary spaces and commas, create new features, save the cleaned file to csv file, 'usedCarListingCleaned.csv'.
3. EDA: extensive explorary data analysis, including lots of visualization to illustrate the distributions of number of listings and prices against different features. Visualize the popular features distribution by plots. Try to answer some questions such as if similar cars in CA and non-CA have different prices, if the price difference exists in CA and TX.
4. Predicting Used Car Price Using ML models: build a xgboost model to predict used car prices, investigate feature importances that affect the car prices.

## Data: 
'usedCarListing.csv': The raw data obtained from web scraping. There are 9655 listings with 15 columns.
'usedCarListingCleaned.csv': The cleaned data after data preprocessing. There are 9652 listings with 22 columns

## Instructions:
You can find all the notebooks in the folder 'notebooks' and two datasets in the foler 'data'. Read the notebooks from 1 to 5 in order to see my whole projects.


Thank you
