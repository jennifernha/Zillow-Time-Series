![cover](./images/california_housing.jpeg)

# Zillow Times Series Analysis
**Author**: Jennifer Ha

## Overview
With their recent susscessful housing investment in New York, our client Stellar Property Group seeks to expand their listings in California, which happens to be the other state with the most Fortune 500 company headquarters besides New York. Our client believes the trends and contributing factors that they saw in New York, especially the continued job growth will continue to increase the home values. The team is looking for recommendations on top 5 zipcodes to invest in California, and this analysis will also provide them with short-term vs. long-term investment decisions.
***
## Business Problem
The goal of this analysis is to identify the top 5 zipcodes for our client to invest in. We have plenty of data to work with but I wanted to be mindful of some finanacial events that happened in the past (e.g. Housing Bubble and Great Despression). Insead of removing these data, I used the coefficient of variantion to take risk into consideration. This is a very common method being used in finance to determine how much volatility, or risk, is assumed in comparison to the amount of retrun expected from investments. I've also selected data in 30-70 quartile to add some variation.

After running some simple time series models, we will use auto_arima on SARIMAX model to determine the best performing parameters for each zipcode. The performance is evaluated using p-value and RMSE, and the recommendation is made based on the predicted ROIs in 1 year, 3 year, 5 year, and 10 yaer.
***
## Data
The original dataset for this analyisis consists of ~14,726 rows and 272 variables of median monthly housing sales prices from April 1996 through 2018 as repored by Zillow. Each row represents a unique zip code indexed with RegioinID, and contains location info and median housing sales prices for each month.
***
## Methods
This project explores 5 different machine learning model types using the SKLearn package: logistic regression, K-Nearest Neighbors, Decision Tree, Random Forest, and Adaboost. Due to overfitting problem, I've decided not to move forward with K-Nearest Neighbors, Decision Tree, and Random Forest models. To further improve the performance, hyperparameter tuning was performed on logistic regression and Adaboost models.
***
## Results
Our result shows that below 5 zipcodes have positive ROI, and therefore, I recommend investing in properties in below zip codes. 

**Zip code 92101 (San Diego):** Buy and sell homes within a year. Can wait loger but no true meaning in that after 3 years.


      Total expected return in 1 year: 10.47%
      Total expected return in 3 year: 14.06%
      Total expected return in 5 year: 14.27%
      Total expected return in 10 year: 14.27%
                                  
                                
**Zip code 91754 (Los Angeles):** Buy and wait for the next 5-10 years. Although can be sold after 5 year term.

      Total expected return in 1 year: 2.6%
      Total expected return in 3 year: 4.72%
      Total expected return in 5 year: 5.32%
      Total expected return in 10 year: 5.54% 
                                  
                                  
**Zip code 92860 (Norco):** Buy and hold for the next 3-5 years. Can wait loger but no true meaning in that after 3 years.

     Total expected return in 1 year: 7.43%
     Total expected return in 3 year: 11.23%
     Total expected return in 5 year: 11.82%
     Total expected return in 10 year: 11.93%
                            
**Zip code 93405 (San Luis Obispo):** Buy, flip and sell within a year. Can wait loger but no true meaning in that after 3 years.

     Total expected return in 1 year: 7.43%
     Total expected return in 3 year: 11.23%
     Total expected return in 5 year: 11.82%
     Total expected return in 10 year: 11.93%

**Zip code 93003 (Ventura):** Buy and hold for atleast 10years. Or forgo this market as the ROI is not too high.

     Total expected return in 1 year: 0.26%
     Total expected return in 3 year: 0.26%
     Total expected return in 5 year: 0.26%
     Total expected return in 10 year: 0.26%



## Next Steps
1. When forecasting home values, there are many other factors to consider besides the actual values. Consider laying in additional data such as population, tax, education, etc.

2. This data goes only up to 2018. We can potentially explore the data with more recent data.


## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jennifernha/NYC-Airbnb-Analysis/blob/main/NewYork-Airbnb-Analysis.ipynb) or review this [presentation](https://github.com/jennifernha/NYC-Airbnb-Analysis/blob/main/Presentation.pdf).
For additional info, contact Jennifer Ha at jnha1119@gmail.com
***
## Repository Structure
```
├── data
├── images                        
├── Zillow_times_series.ipynb   
├── Prensentation.pdf  
├── README.md                           
└── functions.py
  
  