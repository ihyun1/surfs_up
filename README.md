# surfs_up

## Overview
Our client is preparing a presentation on opening a surf shop in Oahu for his board of directors. In his presentation, he wants to provide them with climate analysis to be able to support the viability of the surf and ice cream store being financially sustainable year round. So, we are querying weather data for Oahu from 2010 to 2017 for its temperature recordings in June and December for our client to use in their proposal.

## Analysis
To query our database for the June temperatures of each year, we imported 'extract' from SQLAlchemy in order to specify our filter.
![June_Query_Extract.png](Resources/June_Query_Extract.png)

After transferring our data into a dataframe, we utilized Pandas' describe function to return the summary statistics on the month of June. As shown below, the average temperature was comfortably warm at 74.9 degrees. The coldest temperature recorded in June was 64.0 degrees and the warmest was 85.0 degrees. The standard deviation was 3.26 degrees with 75% of the data recorded being 73 degrees or warmer.

![June_Temp_Stats.png](Resources/June_Temp_Stats.png)


For our December temperature statistics, our average temperature was 71.0 degree, almost four degrees lower. The coldest temperature reached 56 degrees while the warmest was 83 degrees. The standard deviations was larger at 3.75 degrees, attributed to the higher variance of temperatures, with 75% of the data being 69 degrees or warmer.

![Dec_Temp_Stats.png](Resources/Dec_Temp_Stats.png)

## Summary
Given our initial weather analysis, the temperature for the months of June and December are fairly consistent, although December was shown to experience significantly lower temperatures on its coldest days. We believe this data can help to advise the board that the surf and ice cream store would be viable as a year round venture in Oahu given the similar average temperatures, and that about 75% of the recordings for each month being at or above 70 degrees. However, we can further bolster our analysis and gain more insight by performing at least two more queries. 

- The first query is to pull the percipitation summary statistics for each month. This information will greatly help us to forecast our sales, as the higher frequency of rain, the less days the store will be to sell their goods. In the tables below, it is apparent that rain in December is more frequent than in June, at .217 compared to .136, but this information is not enough to deter the opening of the store.

![June_Prcp.png](Resources/June_Prcp.png) ![Dec_Prcp.png](Resources/Dec_Prcp.png)

- The second query is to determine how many stations are recording data and what is the most active weather recording station. In the tables below, June shows a smaller standard deviation, meaning a more consistent temperature than our statistics of all every station's recordings, and in December there is a lower average temperature.

![June_Temp_Station.png](Resources/June_Temp_Station.png) ![Dec_Temp_Station.png](Resources/Dec_Temp_Station.png)

In regard to gathering more data, we suggest finding recordings of the ocean temperatures, and other weather condition recordings such as, cloud cover for these months. This would provide more insightful information of our weather analysis and help to better predict possible consumer interest in surfing in colder temperatures.
