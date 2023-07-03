# citibike-challenge
DU Data Analysis Module 18 Assignment

## Data Prep
**CitibikePy.ipynb** collects, cleans, and merges data from https://citibikenyc.com/system-data on bike stations and individual rides.
It also generates ride statistics for the past year (June, 2022 - May 2023) to compress the ride data which is too large to load into Tableau.
Generated data files are stored in csv form in the **data** folder.

## Data Visualization

Visualization data is presented in the Citibike Activity workbook at https://public.tableau.com/app/profile/amy.paschal/viz/CitibikeActivity/Story1
Tabs contain individual visualizations, 2 dashboards and a story.

The story board contains 4 pages:

### All Stations
Map of all bike stations in the New York City area. Dot sizes represent popularity. The map background layer contains zip code areas labeled with zip codes.

### Station Traffic
In the year ending May 2023, the most popular bike stations by a big margin were those in Jersey City and Hoboken, New Jersey. The maps showing the most popular pick-up and drop-off stations contain a background data layer showing household income. This data is from 2018 and unfortunately the highest category is quite large ($81K - $250K) limiting differentiation. Despite that, it's clear Jersey City and Hoboken are wealthy areas in comparison to the rest of the New York City area which is likely contributing to Citibike popularity.
The service, at a cost of $205 for an annual membership and $19 for a day pass, (reference https://citibikenyc.com/pricing) is a bit high relative to the cost of an inexpensive bike so likely membership and usage is more about convenience that it is about economics.
Folks in Jersey City and Hoboken have the disposable income to pay for convenience.
https://www.nj.com/hudson/2016/03/citi_bike_jersey_city_popular.html


Unsurprisingly, station activity across the year fluctuates with the weather with summer months having the greatest activity and winter months the lowest.

### Ridership Activity - Volume
Like station activity, ridership fluctuates with the weather. Summer months have the most rides and winter months the least. Casual usage peaks at approx. 40% in the summer months and drops to its lowest, about 20%, in the winter months, with those who have paid for the annual membership the most willing to use the service in the colder months.

### Ridership Activity - Trip Time and length
More surprisingly, average rides are short, fluctuating between .65 miles and .75 miles, and between about 8 and 15 minutes, throughout the year. Peak hours for bike usage are around 8 AM and 6 PM for member riders. It appears that these customers are using the bikes as a leg in their commute, perhaps to get from public transportation to work and back to public transportation again, rather than using the bike for their entire commute. Perhaps there are no bike stations near their homes or the commute distance is too long to have the time or stamina to bike the entire distance.

Peak ride hours vary slightly between members and casual users. Members have clear peaks at 8 AM and 6 PM. Casual riders have a steady increase from 5 AM to 6 PM and then a steep drop off. Perhaps unplanned trips increase as the day wears on because time and energy become more valuable as folks get more behind on their plans for the day.

## Data Inconsistency - Recommendation
There appears to be no station ID that is consistent between the station information data and the ridership information data. Hence, I was forced to use the station names in merging the data.
Station names, a text string. are also not consistent so I had to do some name matching and some dropping of data.

Recommendation: I recommend to Citibike IT to create a short string ID for all the bike stations and to use that same data in all the files referencing bike stations for easy and accurate matching of data.
