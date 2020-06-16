# ETL_project
# Ashton Preble, Brittany Hethcock, Jake Andrasovsky, Kate Como

#Project Datasets: Wine Quality vs Location; Analysis that *would* be done: Does better wine correspond to specific weather? 


Extract  - 

Our main data source was a CSV file from Kaggle.com. The data set was made up of 13 columns and 129,972 rows. The information in this CSV file are wine ratings from all over the world. Our second data source was from Google API places. We used a for loop and API call to gather Lat and Long coordinates in order to match to a wine location.  

Transform - 

After taking the data from a CSV and putting it into a data frame, we needed to clean it up by removing several columns that were not necessary for our comparison, filtered non-US data, and reset the index.  With our second data set we grouped by the state of each winery, added API detail, cleaned the data and joined them together. We renamed columns in both tables to be more descriptive. 

Load -  

The database Wasted Away in Wine Land is hosted on Postgres and comprised of 2 tables the  state_df and the us_transformed_wine_df. There is a third table on the server with this information joined as one called the wine_state_df.  The state_df is a table lists the states containing the wineries and their relevant latitude longitude coordinates. The province is a foreign key in our second table the us_transformed_wine_df containing the wine quality data & winery information. We chose to use SQL as it best fit our tabular data structure.


Limitations - 

Due to the size of the data set pulling average weather data was not possible with a google or free weather API. 
