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