# Realtor_Data
USA real estate data analytics and predictions. Data Provided from Kaggle [link](https://www.kaggle.com/datasets/ahmedshahriarsakib/usa-real-estate-dataset). This Data set contains real estate data web scrapped from [Realtor.com](https://www.realtor.com/). Including House Listing prices, baths, acres, beds, state, zip code and many other features of the houses. Predictions will be for the house prices and the analytics will be comparing the house features, locations, and prices. 


## Average House Prices 
Since there are houses that exceed 1 million they act as outliers for the data and would skew the mean/avg prices. with this, in mind I've capped to only show the houses that are on the market for no more than $1,000,000. After doing this it brought the numbers a lot closer together for comparison New Hampshire and Rhode Island are the top two only separated by a $10,000 difference. After seeing this graph I'd like to compare the individual cities within New Hampshire. 
![AvgStatePrices](https://i.gyazo.com/769a042985eb70761f076e6a51da06f1.png)



## Average New Hampshire House Prices
Within the first graph, New Hampshire was the state with the highest average house prices. To Compare let's see which cities have the highest and lowest average prices. Keep in mind that not all cities may have the same amount of houses on the market, and this could skew the prices slightly. For example if there is only one house on the market for $100,000. The city will show that the average price is 100,000 since it's only one house. Whereas a city with 10 houses ranging from 100,000 to 1,000,000 would show a more average price.
![AvgNewHam](https://i.gyazo.com/3b31da8b443953a84efb843489bd1936.png)


## House Price Ranges By State
This can help us understand where the significant amount of house prices are for each state. For example you 
are more likely to get a cheaper house in Puerto Rico and Vermont compared to road island New Hampshire etc. We can also see which states have fewer houses on the market and which have more. New Jersey, South Carolina, Tennessee, and Virginia all have a very little amount of houses on the market that they don't have as large of an interquartile range as the other states. One thing to note is that although Puerto Rico has the lowest prices there are significantly more outliers than the other states meaning that some houses can be a lot more expensive than the other states. 
![HousePriceRange](https://i.gyazo.com/43510139886e95e08bb01ec118337668.png)



# Machine Learning 
With the dataset not being completely evenly distributed between each state. I've decided for the better of the model and the scores to use only the top four states. These are Connecticut, Massachusetts, Puerto Rico, and Rhode Island. The models are regression models. However, with these datasets having a lot of features instead of removing them and losing data on the houses for predictions wouldn't be ideal. So, using boosters like LGBMRegressor help the train and testing scores.

### Kneighbors Model
At first, I tried just a normal Kneighbors model and by no surprise, the runtime took a lot longer than needed, and the scores were not up to par. This is due to the data having a lot of features. However, to combat this using boosters such as LGBM can fit the data faster and have better scores with the number of features in the data. 
Kneighbors Scores\
Training: 0.55\
Testing: 0.22


### LGBM Model 
Since the Kneighbors model didn't perform that great using a booster like LGBM will help a good bit on the scores. 
just a base LGBM model gave scores of Training: 0.60 and Testing: 0.58. After running the default model I tried to use a gird search to see if any parameters would make the model's scores improve however the default parameters produced the highest scores. This Graph below shows all the error and r2 scores for the base LGBM model. The RMSE states that the data is roughly 70,000 off now which is a lot to be missing for predicting the price of a house. If you were to use this model to tell you what your house would be worth or to price match in some way. That could mean losing or overshooting the price of the house by almost 70,000. This could be fixed by just having more data there are millions maybe even billions of houses in the world so adding to the 12,000 houses used for the prediction and adding more with similar features would only help the predictions. I would rate these model scores as fair they aren't the best but they also aren't so far gone that you would just throw them out they could still be used but defiantly could be approved upon. 

![ModelScores](https://i.gyazo.com/210958ab6e7bd570cafb5f00518911db.png)
