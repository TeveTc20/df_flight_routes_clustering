# Data Science flight routes clustering 
# Project overview

* Scraped 99 routes from TLV to different locations - every route contains samples of latitude and longitude.
* Smoothed the data using Kalman filter.
* Calculate dtw distances to see the difference between every 2 sequences.
* Cluster using K-means, Hierarchical and GMM.
* Analyzed patterns of subsequence.

# Code and Resource Used
**Python Version:** 3.11.1
**Packages:** Selenium , Pandas , Numpy , Matplotlib , Seaborn , sklearn.

## Web scraping
Scraped over 40,000 rows of flight routes samples which amouts to 99 different flight routes sequences, we got the following:
* Route
* Airline Name
* Flight number
* Type of aircraft
* Date
* Time
* Latitude
* Longitude
* Course
* Mph
* Feet
* Rate
* Reporting Facility

# Data Cleaning
After scraping the data , needed to smooth the data due to wrong sampling, use Kalman filter to smooth the data.

# EDA
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/airline.png "Airline histogram")
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/aircraft.png "Aircraft histogram")
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/date.png "Date histogram")
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/mph.png "MPH histogram")
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/europe_flights.png "Map or flights to Europe")
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/asia_flights.png "Map or flights to Asia")
![alt text](https://github.com/TeveTc20/ds_flight_routes_clustering/blob/main/images/america_flights.png "Map or flights to America")

# Clustering models
Tried 4 different models:
* K-means from scatch
* Hierarchical from scratch
* Hierarchical from sklearn
* GMM from sklearn
  
# Analyzing subsequence patterns
* Splitted the flights for 3 continents: Europe, Asia and America
* Calculated for every sequence the distance and angle differences between two consecutive point to check for unusual pattern
* After finding the routes, analyzed the spots where the angle and distance difference was unusal and reaching conclusions
