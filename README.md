# python-api-challenge
Module 6 Challenge


# Description
Data scientists are only as good as the data used. With the internet's vast reaches, data can be pulled from every crevice of the network of networks. The combination of the requests module, API calls and JSON allows us to grab avaiable data at the click of a button (and some light coding script). The assignment is an exercise in making successive API calls to a data source and using JSON to fill out a Pandas dataframe.

In this repository, you will find two Jupyter notebooks, WeatherPy and VacationPy, as well as an Images folder and an output_data folder. The WeatherPy notebook contains script that makes calls to the OpenWeather API to grab and store weather information for a list of randomly generated latitudes and longitudes. WeatherPy also uses the citipy module to determine the city based on those latitudes and longitudes. The weather information is saved as a CSV file in the output_data folder.

The script continues to create four scatter plots with Pandas and Matplotlib:
    - Latitiude vs. Temperature
    - Latitude vs. Humidity
    - Latitude vs. Cloudiness
    - Latitude vs. Wind Speed

Then the script uses linear regression from the scipy module to model the relationship between latitudes, separated out by northern and southern hemispheres and those same four weather attributes. Images of the all the plots are saved in the Images folder.

The VacationPy notebook takes the data gather from WeatherPy filtered by my ideal weather conditions: maximum temperature ranges from 70 to 75 degrees Fahrenheit, wind speed is less than 8 mph and cloudiness is less than 10%. A breeze and some nice clouds to look at are definitely underrated. VacationPy uses the gmaps module to create a heatmap based on humitidy. VacationPy also makes calls to the Google Place API to gather and store hotel names for the cities that meet my ideal weather conditions. The notebook subsquently adds markers for the hotels as well as a clickable info box.

# Observations
1. Temperature in the northern hemisphere tends to have a negative correlation with latitude, i.e. temperature decreases as you move away from the equator. The r value is 0.63, indicating a moderate strength of correlation.
2. Temperature in the southern hemisphere tend to have a positive correlation with latitude, i.e. temperature increases as you move closer to the equator. The r value is 0.80, indicating a strong strength of correlation.
3. There appears to be no correlation between humitidy and latitude. The r values for both northern and southern hemispheres are less than 0.3, indicating little to no correlation.
4. There appears to be no correlation between cloudiness and latitude. The r values for both northern and southern hemispheres are less than 0.3, indicating little to no correlation.
5. There appears to be no correlation between wind speed and latitude. The r values for both northern and southern hemispheres are less than 0.3, indicating little to no correlation.

# Requirements
To run the script in the two Jupyter Notebooks, you will need the following:
    - API keys to OpenWeather API and Google Maps/Places API
    - citipy module
    - jupyter gmaps extension



