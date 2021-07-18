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
```pyber_data_df = pd.merge(ride_data_df, city_data_df, how="left", on=["city", "city"])```. I then created Series using the ```.groupby()``` method to create 3 series and used those to calculate totals and averages.
I then combined those series into the Pyber Summmary Dataframe, depicted below.




### Multiple-Line Chart


## Summary
Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types
