# Python API 

Data's true power lies in its ability to answer questions definitively. In this repository I take what I've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

## Part I - WeatherPy

For part one I create a Python script to visualize the weather of 500+ cities across the world of varying distance from the equator. To accomplish this, I will be utilizing a [simple Python library](https://pypi.python.org/pypi/citipy), and the [OpenWeatherMap API](https://openweathermap.org/api) to create a representative model of weather across world cities.

To start I created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot I added a sentence or too explaining what the code is and analyzing.

The second part is a linear regression on each relationship, only this time I separate them into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each pair of plots I explain what the linear regression is modeling such as any relationships you notice and any other analysis I deemed necessary.

### Part II - VacationPy

* I created a heat map that displays the humidity for every city from the part I.

* Then I narrow down the DataFrame to find your ideal weather condition:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

  * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.


* Using Google Places API I find the first hotel for each city located within 5000 meters of your coordinates.

* I then plot the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

### Copyright

Trilogy Education Services © 2019. All Rights Reserved.
