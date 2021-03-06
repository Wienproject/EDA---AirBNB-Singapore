# Exploratory Data Analyst---AirBNB-Singapore

Exploratory Data Analysis AirBNB – Singapore

## Outline of the Analysis
- Define Problems and Goals
- Getting data and Data Cleansing
- Analyzing and getting data insight
- Insight Visualization

## Problem:
Acting as one of AirBNB's Data Scientist, multiple insights are needed to expand our business area.
In that case, few factors have be discovered:
1. Where the most optimal location to make an expansion is.
2. Best estimated price on each location.
3. Which room type have the highest occupancy rate for each location

## Goal:
Exploring data to figure out insights that will help solving defined problem.

Data Source:
•http://insideairbnb.com/get-the-data.html - Singapore - listings.csv

![Data Frame](Picture1.png)
The Data consists of 7323 rows x 15 columns with columns:
- Id, name, host_id, host_name, neighbourhood_group, neighbourhood, latitude, longitude, room_type, price, minimum_nights, number_of_reviews, last_review, reviews_per_month, calculated_host_listings_count, availabity_365 

## DATA CLEANSING

  Handling Missing Value
  
![This figure shows which columns has Missing values](Picture2.png) 

- 1 row of missing value in column ‘name’
- 22 rows of missing values in columns ‘host_name
- 2835 rows of missing values from columns ‘last_review’ and ‘reviews_per_month’ 

![Filling missing Values](Picture6.png)

For the columns ‘last_review’ and ‘reviews_per_month’ we fill the NaN values with 0 (zero).
Because the rows that have NaN values on both columns are the rows the have 0 Number_of_reviews
So we can conclude that with 0 Number_of_reviews there will also be 0 last_review and reviews_per_month

![Missing Value](Picture7.png)

For the missing value in column ‘name’ we fill in the value ‘Unknown’
For the missing value in column ‘host_name’ we fill in the value ‘Classified’

## DATA ANALYSIST

In order to approach to the Analysist,  first thing is determining what are the most critical factors to expand our business area.

4 most important factors are needed to be identified, which are:
Neighbourhood_group and Neighbourhood
Price
Occupancy Rate
Room Type

*Neighbourhood_groups and Neighbourhoods gives us basic information about locations in Singapore. By combining data based on their neighbourhood_groups / neighbourhoods we will gain information on which neighbourhood_groups / neighbourhoods should we do an expansion

*Price is very important because usually price determines the occupancy rate of a room, people usually chose the room with the cheapest price.

*Occupancy Rate on the other hand gives insights to us to know in which location of Singapore does AirBNB has the highest occupancy rate, so that location could be the best fitted location to doing an expansion

*Room Type because we want insights on what type of room should we make an expansion on.

![Pie Chart](Picture9.png)
![Ammount of data variances](Picture10.png)

The first part of the analysist is tring to find insights from the Neighbourhood_group data. We want to know how is the spread of room in Singapore base on their neighbourhood_groups available in Singapore. To visualize this data Pie chart is used.

According to this pie char, it is to see, that the majority of AirBNB location is in Central Region with 80.1% The amount of all airBNB unit in this area is far beyond any other Regions, which not even 10%. City center, tourist attraction (i.e. Marina Bay Sand, Garden by the bay, and Universal studios), and location of the majority of business district are just a few example, why Central Region is the most favorable Region to stay in Singapore.

![Price mean and Occupancy Rate Percentage](Picture11.png)

Then the next observfation is finding the average Price and Occupancy Rate Percentage of rooms based on their neighbourhood_group, the picture shows python code and results.

![Average Price in each neighborhood group](Picture12.png)

Based on the graph is concluded:
Central Region has the highest average price of rooms
North Region has the lowest average price of rooms

![Occupancy Rate Percentage in each neighbourhood group](Picture13.png)

Nevertheless this graph shows:
The highest average Occupancy Rate of rooms is at the North-East Region
The lowest average Occupancy Rate of rooms is at the Central Region 

![Pie Chart](Picture16.png)
![Amount of room type in Singapore](Picture17.png)

The last part of our analysis is trying to find insights from the Room Type Data. We want to know how is the spread of room_types in Singapore base on their respective types. To visualize this data Pie Chart is being used.

This pie chart shows, that most stay are either entire home/apt or private room, with 47.4% and 42.8%, whereas hotel room and shared room come as 3rd and 4th most favorable respectively, with 6.2% and 3.6%. Most of our partner rent us their entire home, entire apt, or private room, which can be seen via this pie chart.


![Histogram 1](Picture18.png)

This code is to check the average of Price and Occupancy rate of each room type based on the whole data.

![Histogram 2](Picture22.png)

The next step is observing to be more specific the average Price and Occupancy Rate of each Room_Type based on their Neighbourhood_group, the picture shows the used code and the results. Nevertheless Nan is seen as Missing values on some columns. Within this Neighbourhood_group, the corresponding Room_type is barely not available.

![This Barplot shows the average Price of each room_types on every Neighbourhood_group](Picture19.png)

This Barplot shows the average Price of each room_types on every Neighbourhood_group.

Overall listed price trend in each neighbourhood group are:
1. Entire Home/Apartment as the highest, (Although in North-East Region it shows that Hotel Room has higher average price)
2. Followed by Hotel Room, 
3. Private Room and 
4. Shared Room respectively. 

Their average price difference is determined by the amount of facilities, room area and privacy. For example an apartment has more plus point on those aspects than the shared rooms, with more facilities and also a bigger place to stay, The price is definitely higher.

![This figure shows the average Occupancy Rate Percentage of each room_types on every Neighbourhood_group](Picture20.png)

This figure shows the average Occupancy Rate Percentage of each room_types on every Neighbourhood_group.

- The bar chart above shows that the overall trend of occupancy rate in each neighbourhoods group differs, showing that there are DIFFERENT demand in room type between each region. 
- In Central and North Region, the occupancy rate are almost the same between each room types (But North Region doesn't have hotel room type). 
- In East and North-East Region, the highest occupancy rate is the shared room type followed by the entire home/apt and private room. 
- While the highest in West Region is the private room followed by entire home/apt and shared room. 
- However the occupancy rate of hotel room in every region is the lowest.

## CORRELATION - DATA VISUALIZATION

![Correlation](Picture21.png)

### DATA ANALYSIST - CORRELATION

Based on described figure:
1. Neighbourhood_Group = Central Region
Assumed there is a slight positive correlation in Central Region between Occupancy rate and Price, however it is not significant. 

2. Neighbourhood_Group = West Region
In West Region is also shown, that in this region also has a weak positive trend line, however it is still moving upwards.On the other hands, 

3. Neighbourhood_Group = East and North – East Region
Both East and North - East Region shows, there is negative correlation between occupancy rate and price of the room, especially for North-East Region the trendline is shown stronger. 

4. Neighbourhood_Group = North Region
Finally, North Region has the least ammount of our unit, which the correlationis hard to describe. In order to provide more accurate data, more samples is still needed


## CONCLUSION

AirBNB is an online vacation rental business, which is growing strong recently. Some datasets are strongly demanded in order to provide a decent insight in terms of developing our business area. 

This provided dataset might be one of the right tools to investigate new business potential. There are some important factors, given by this dataset, i.e. occupancy rate percentage and price. These are such vital factors to define a potential new business area. According to our analysist and investigation it is shown that these 2 factors are not strongly correlated. 

Although, In some region like Central region and West Region the Occupancy Rate Percentage and Price shows slight positive correlations, on the other side negative correlation are also shown by East and North-East Region. 

From our analysis we also think that there are still plenty of factors that can affect the price or occupancy_rate of a room, for example number of facilities, room_width, etc In conclusion, there are still lots of existing factors that will often relatively influenced price and occupancy rate. These supplementary computations with complete data sources might potentially provide better understanding to provide a decent insight in addition to our business development programs.

## RECOMMENDATION

According to our research, Central Region is simply loved by tourists with its things, i.e. lots of tourist attractions, city center, major business districts and also Marina South area. You can find whatever you want in Central Region. However the stay price is relatively high in comparison to the other Regions. 

Based on the analysis and visualizations of Airbnb Singapore dataset, we see the potential for expansion in the North-East Region, especially in the neighbourhood of Ang-Mo-Kio, Punggol, Sengkang and Serangoon which showed high occupancy rate. We recommend expansion on those regions with Shared Room type as the most preferred one in those region. 

Nevertheless we saw North-East Region as a new potential to expand our business coverage. Relatively high occupancy area with a decent price could be a unique selling point, that this region could provide. It is also located not so far from the Changi International airport is also big selling point as well. 
