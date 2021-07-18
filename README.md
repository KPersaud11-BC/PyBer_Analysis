# PyBer_Analysis by Kieran Persaud

## Overview of the Pyber Ridesharing Analysis
V. Isualize, the CEO of Pyber, a Python-Based Ridesharing company, tasked me with creating a summary Dataframe of the ride-sharing data by city type and a multiple-line graph depicting the total weekly fares for each city type. The two deliverables were created from the csv files for city data and ride data, using Pandas to create and merge the csv's into various Dataframes, and Matplotlib to plot the results.

## Resources
- Data Sources: city_data.csv, ride_data.csv
- Software: Anaconda 4.10.1, Pandas and Matplotlib Libraries, PythonData kernel; Jupyter Notebook
 
## Results
Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types.

### Summary DataFrame
After reading in 2 csv files and creating DataFrames of each, I merged the data into a single DataFrame using 
```pyber_data_df = pd.merge(ride_data_df, city_data_df, how="left", on=["city", "city"])```. I then created Series using the ```.groupby()``` method to create 3 series and used those to calculate average fare per ride and per driver.
I then combined those series into the Pyber Summmary Dataframe, depicted below.

![Summary_DataFrame](https://user-images.githubusercontent.com/84286467/126079186-e9fabfd9-c394-44c4-a1f9-14e87b8b3607.PNG)

Rural areas account for the lowest total rides, total drivers, and total fares. However, they boast the highest average fare per ride and per driver compared to urban and suburban areas. The inverse is true for urban areas. They account for the highest total rides, total drivers, and total fares, but the lowest average fare per ride and per driver.

### Multiple-Line Chart
Again using the ```.groupby()``` method on the ```pyber_data_df```, I created a new DataFrame showing the sum of the fares for each date. Using the ```.pivot()``` function, I modified that Dataframe with "date" as the index and city type as the columns. The analysis viewed the timeframe between January 1, 2019 and April 29, 2019. The table was filtered using the ```loc``` method for that date range. Finally, the dataframe was resampled to show total weekly fares by city type. Below is the resulting plot.

![Pyber_fare_summary](https://user-images.githubusercontent.com/84286467/126079765-35844a83-0e1a-4ecc-9725-2445e2e29856.png)

Here are some noteworthy points that can be taken from the graph:
- There are increases in total fare revenue in urban and suburban cities for January, and decreases in rural areas. 
- There is a decrease in total fare revenue across all city types in the last week of February.
- Fare revenue for Suburban cities is relatively flat for the month of March.
- In the month of April, there is a decrease in rural area fare revenue, and a significant increase in suburban fare revenue. There is a slight decrease in urban fare revenue.

## Summary
Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types
