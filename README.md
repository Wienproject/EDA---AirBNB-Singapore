# EDA---AirBNB-Singapore

Exploratory Data Analysis AirBNB – Singapore

Outline of the Analysis
- Define Problems and Goals
- Getting data and Data Cleansing
- Analyzing and getting data insight
- Insight Visualization

Problem:
Acting as one of AirBNB's Data Scientist, multiple insights are needed to expand our business area.
In that case, few factors have be discovered:
1. Where the most optimal location to make an expansion is.
2. Best estimated price on each location.
3. Which room type have the highest occupancy rate for each location

Goal:
Exploring data to figure out insights that will help solving defined problem.

Data Source:
•http://insideairbnb.com/get-the-data.html - Singapore - listings.csv

![Data Frame](Picture1.png)
The Data consists of 7323 rows x 15 columns with columns:
- Id, name, host_id, host_name, neighbourhood_group, neighbourhood, latitude, longitude, room_type, price, minimum_nights, number_of_reviews, last_review, reviews_per_month, calculated_host_listings_count, availabity_365 

DATA Cleansing
  Handling Missing Value
  
![This figure shows which columns has Missing values](Picture2.png) 

- 1 row of missing value in column ‘name’
- 22 rows of missing values in columns ‘host_name
- 2835 rows of missing values from columns ‘last_review’ and ‘reviews_per_month’ 

![Filling missing Values](Picture26.png)
For the columns ‘last_review’ and ‘reviews_per_month’ we fill the NaN values with 0 (zero).
Because the rows that have NaN values on both columns are the rows the have 0 Number_of_reviews
So we can conclude that with 0 Number_of_reviews there will also be 0 last_review and reviews_per_month


