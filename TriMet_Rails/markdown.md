### TriMet MAX Light Rail Data
***

#### Objective

This was a project I took on while participating in the Portland Data Science Group meet up. The goal was to explore the data set and attempt to answer questions and/or provide insights from the data. The questions that I began to explore with my group all focused around the delay of the light rails, such as which routes had the highest delays, the time of day with the most delay, and stops that experience the most delay.

#### Steps Taken

We split up into groups based on the questions we were most interested in pursuing about the data. Meeting once a week over the course of 4 weeks we would share our progress and findings and collaborate during the meetings as well as over Slack. The data files were in the form of .csv files and together comprised a very large data set with 9,241,236 entries. In order to work with the data I had to learn how to use the pandas Python library and worked using Jupyter notebooks. The pandas library is able to read in csv files and create DataFrame objects that can be manipulated much like tables in SQL. I struggled initially learning the syntax and structure of pandas DataFramesI also began familiarizing myself with the Seaborn library as well as using a Google Maps API key so that I could produce plots and data visualizations. 

#### The Result

We were able to find that the Blue MAX line had the most overall delays as well as the highest average delay time. The stops with the worst delays appeared to be in Gresham. Here are just a few of the summary statistics that I plotted for reference:

![Alt text](TriMet_Rails/total_counts_route.jpg?raw=true "total_counts_route")

![Alt text](TriMet_Rails/mean_delays_route_plot.jpg?raw=true "mean_delays_route_plot")

![Alt text](TriMet_Rails/median_delays_route_plot.jpg?raw=true "median_delays_route_plot")

It is important to note, however, that the Blue line is also the longest of the MAX routes and will thus compound its figures. Because of this we also began to try querying the data by route segments using the rail’s sign messages. 

Attempting this finer granularity, we began to explore the delay trends over the time of day and produce a temporal heat map for each route segment. We used Seaborn to plot the heatmap:

![Alt text](TriMet_Rails/segment_delay_heatmap.JPG?raw=true "segment_delay_heatmap")

The gaps of data in the plot were a concern. After doing some investigative querying I was able to determine that there were, indeed, gaps in the data provided by TriMet with no entries for those time intervals. This turned out to be a good exercise in data validation, although we were disappointed that we were not able to provide any truly representative temporal trends. 

After reaching this obstruction, I decided to look at plotting the locations of the delay events:

![Alt text](TriMet_Rails/delay_stop_location.JPG?raw=true "delay_stop_location")

It was interesting to see the routes of the MAX lines plotted out by the delays. What was more interesting was the strange alternating trend in the mean delay value. In the plot you can see the value of the delay alternating in extremity in multiple lengths of routes. It would be interesting to see what exactly is causing this trend.

Finally, I grabbed a Google Maps API key so that I could create a heatmap that overlays onto an actual map to provide a better geographic understanding:

![Alt text](TriMet_Rails/api_delay_heatmap.JPG?raw=true "api_delay_heatmap")

Between both heatmaps, it is pretty obvious that you will see a lot of delays in the downtown area simply due to the higher activity. 

Overall I found this to be a very good exploratory data project and enjoyed learning some new toolsets. The data was fairly robust and could easily be further explored. Combining it with additional data such as weather or economic information would be sure to provide more interesting insights.

[Return to portfolio](https://github.com/zfregin/portfolio)
