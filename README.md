# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
This project explored the City Bikes API, Foursquare API, and Yelp API by taking the data and creating a regression model to better understand how different points of interests affected bike availabity at different stations in Madrid. Data was stored in a SQLite database.

## Process
### Step 01
Collecting Data for city bikes. I gathered data on the bike stations in Madrid from the CityBikes API. I parsed the JSON response, extracted the bike station data, normalized the data into a DataFrame, and then cleaned up the data, retaining only desired columns. I then parsed the results into a CSV file.
###  Step 02
Collecting data for points of interest using Foursquare and Yelp APIs. I collected the API responses to extract details of interest, and then converted the information into DataFrames that were stored into CSV files.
###  Step 03
Merging data. In order to query all the information I pulled, I had to put it into one file that we can base our regression models on. I used the Pandas library to merge the data, then cleaned any null values.

### Step 04
Using libraries to create visualizations in order to answer some EDA questions. This allowed me to familiarize myself with what the data was saying.

###  Step 04
Storing data in a SQLite database.

###  Step 05
Building the model. This is where I analyzed if there was a relationship between bike availity and the previously explored points of interest.

###  Step 06
Intepreted results. I examined the regression models and determined whether the points of interest data showed any significant results that answered any questions about how these points of interest correlated to bike availability at these stations.


## Results
When comparing the Yelp and FourSquare APIs, I found that Yelp had a far more comprehensive API to explore so I based most of my data collection on that API. It had a richer insight on ratings of restaurants, which became an valuable point of interest for my model moving forward.

When exploring the data visualizations, I found that there was not any obvious relationship between a bike stations' distance to a restaurant and the restaurants' ratings. This means that no matter how far or close a restaurant was to a station, it did not affect the number of bikes available. Spanish food was the most common restaurant category, which makes sense giving the geographical location explored. The most popular restaurant in terms of review counts is Chocolateria San Gines, which was nearest to the Plaza Conde Suchil Station.

Though the scatterplot suggested no relationship between restaurant distance and bike availability, I was able to explore this futher using a regression model. Results of the regression model suggested that there indeed was no relationship between distance and free bikes, but restaurant rating may be correlated with bike availability. However, the model also suggested that more data is needed to improve the model.


## Challenges 
API limits (especially regarding Yelp) was a big challenge I had to manage. I had to carefully manage the requests I was making. Interpreting the results of the regression model was difficult as well as it was difficult to turn numerical responses into a tangible explanation for the relationship between different variables.

## Future Goals
(what would you do if you had more time?)
Explore other points of interest. If I could exand the dataset to be more comprehensive and therefore improve my model, I'd like the explore the relationship between restaurant rating and bike availability in more depth to determine if there is a true relationship between the two.
