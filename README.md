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
Our winning model is the last model we ran in this project, which is a gradient boosting model with hyperparameter tuning to improve precision. This model is the best as we were able to increase the precision by 18.5% with almost no sacrifice to the accuracy and ROC-AUC score. This model also shows that it has the highest threshold when deciding whether a listing is valuable or not, allowing the least room for errors for the Airbnb marketing team when promoting the top 25% listings.

![result](./images/results1.png)

![graph](./images/results2.png)
***
## Next Steps
1. **Understand what features make a listing valuable.** Now that we have a model that can help the team to select top 25% listings with the best weighted review scores rating, we can also potentially explore different features to understand which ones have the most impact. As a medium that connects the hosts and the guests, it would be very beneficial for the team and the company to know what connects these two audiences. Having more valuable listings and having a better standard of their listing selections will attract more guests to find a place to stay through Airbnb.

2. **Re-visit over-fitting models and think about how we can reduce the over-fitting.** While we were able to create a model that we could rely on, I think there is still a chance to further improve the models that we didn't move forward with or that didn't yield the best performance. We won't know the answer until we finish exploring but this can be an interesting study as the best model we have is not the most perfect model.

3. **Consider expanding this project to make predictions using global data.** This project explores the last 12 months of listing data in NYC only and I believe we can expand the business learnings by including listing data from other cities across the globe. Airbnb is a global company that many people use, and there are many other cities people visit every year. The best model we built from this project might not be directly applicable but the iteration process can still be applied. Such a process will help Airbnb to select the most valuable listings very efficiently, which will also provide a better understanding with their overall listings as well as the valuable listings globally.


## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jennifernha/NYC-Airbnb-Analysis/blob/main/NewYork-Airbnb-Analysis.ipynb) or review this [presentation](https://github.com/jennifernha/NYC-Airbnb-Analysis/blob/main/Presentation.pdf).
For additional info, contact Jennifer Ha at jnha1119@gmail.com
***
## Repository Structure
```
├── data
├── images                        
├── NewYork-Airbnb-Analysis.ipynb   
├── Prensentation.pdf  
├── README.md                           
└── functions.py
  
  