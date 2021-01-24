# Python API Challenge
# What's the Weather Like? Should I plan a vacation?


# Part I - WeatherPy

In this project, we'll be creating a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, we'll be utilizing a simple Python library, the OpenWeatherMap API,  to create a representative model of weather across world cities.
Our first requirement is to create a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot add a sentence or too explaining what the code is and analyzing.

Our second requirement is to run linear regression on each relationship, only this time separating them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots explain what the linear regression is modeling such as any relationships we notice and any other analysis we may have.

Our final notebook must:

* Randomly select at least 500 unique (non-repeat) cities based on latitude and longitude.
* Perform a weather check on each of the cities using a series of successive API calls.
* Include a print log of each city as it's being processed with the city number and city name.
* Save a CSV of all retrieved data and a PNG image for each scatter plot.


### Observable Trends - Northern and Southern hemisphere Latitude vs Max Temp

As we move away from the equator, we observe a decrease in temperature.
The r-squared value of northern hemisphere is 0.44 which means that the model explains almost all the variability of the data around its mean.
As per the Southern hemisphere plot, we observe that as we approach towards the equator, the temperature increases.
The r-squared value of southern hemisphere is 0.54 which means that the model explains almost all the variability of the data around its mean.


### Observable Trends - Northern and Southern hemisphere Latitude vs Humidity(%)

Northern hemisphere is more humid than southern hemisphere.
The r-squared value of northern hemisphere is 0.0126 and that of southern hemisphere is 0.00105 which means that the model failed to explain the variablity of humidity.



### Observable Trends - Northern and Southern hemisphere Latitude vs Cloudiness(%)

Nothern hemisphere is more cloudy than southern hemisphere.


### Observable Trends - Northern and Southern hemisphere Latitude vs Wind Speed (mph)

In northern hemisphere, most cities are having wind speed in the range between 0 mph to 15 mph.
In southern hemkisphere, most cities have wind speed between 0 mph to 10 mph.

# Part II - VacationPy

In this part, we will be working with weather data to plan our future vacations. We are using jupyter-gmaps and the Google Places API for this part of the project.

* Create a heat map that displays the humidity for every city from the part I of the project.
* Narrow down the DataFrame to find ideal weather condition. For example:

        * A max temperature lower than 80 degrees but higher than 70.
        * Wind speed less than 10 mph.
        * Zero cloudiness.
        
* Drop any rows that don't contain all three conditions. Be sure the weather is ideal.
* Using Google Places API, find the first hotel for each city located within 5000 meters of the City coordinates.
* Plot the hotels on top of the humidity heatmap with each pin containing the Hotel Name, City, and Country.

