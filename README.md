# ETL_project
# Ashton Preble, Brittany Hethcock, Jake Andrasovsky, Kate Como

#Project Datasets: Wine Quality vs Location; Location vs Weather - Analysis that *would* be done: Does better wine correspond to specific weather?


Extract  - 

Our main data source was a CSV file from Kaggle.com. The data set was made up of 13 columns and 129,972 rows. The information in this CSV file are wine ratings from all over the world. Our second data source was from Google API places. We used a for loop and API call to gather Lat and Long coordinates in order to match to a wine location.  

Transform

After taking the data from a csv and putting it into a data frame, we needed to clean it up by removing several columns that were not necessary for our comparison. We grouped our data by “province”. With our second data set we grouped by the average score of each wine. We then cleaned that data and joined them together. We performed transformations and joined the data to create a new dataset. We cleaned it up by dropping some columns and setting a new index. We renamed some columns to be more descriptive. We filtered out any data that was not from a US winery. 
Using the latitude and longitude given in our dataset, we were able to use Google’s weather API to create another data frame and compare by location. We performed further transformation with this new data by setting the index, dropping columns we didn’t need, and then renaming the remaining columns. 
