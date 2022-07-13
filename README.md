# World_Weather_Analysis

## Project Outline
There is no standard analysis for this project; this documentation includes coding notes and outlines only of the basic and challenge project plans.

### Basic Project Plan <sup>(as directly from Mod 6.1.2)</sup>
Here's an outline of your project plan:
- Task: Collect and analyze weather data across cities worldwide.
- Purpose: PlanMyTrip will use the data to recommend ideal hotels based on clients' weather preferences.
- Method: Create a Pandas DataFrame with 500 or more of the world's unique cities and their weather data in real time. This process will entail collecting, analyzing, and visualizing the data.

Your analysis of the data will be split into three main parts, or stages.
1. Collect the Data

>- Use the NumPy module to generate more than 1,500 random latitudes and longitudes.
>- Use the citipy module to list the nearest city to the latitudes and longitudes.
>- Use the OpenWeatherMap API to request the current weather data from each unique city in your list.
>- Parse the JSON data from the API request.
>- Collect the following data from the JSON file and add it to a DataFrame:
>> - City, country, and date
>> - Latitude and longitude
>> - Maximum temperature
>> - Humidity
>> - Cloudiness
>> - Wind speed

2. Exploratory Analysis with Visualization

>- Create scatter plots of the weather data for the following comparisons:
>>- Latitude versus temperature
>>- Latitude versus humidity
>>- Latitude versus cloudiness
>>- Latitude versus wind speed

>- Determine the correlations for the following weather data:
>>- Latitude and temperature
>>- Latitude and humidity
>>- Latitude and cloudiness
>>- Latitude and wind speed

>- Create a series of heatmaps using the Google Maps and Places API that showcases the following:
>>- Latitude and temperature
>>- Latitude and humidity
>>- Latitude and cloudiness
>>- Latitude and wind speed

3. Visualize Travel Data

>Create a heatmap with pop-up markers that can display information on specific cities based on a customer's travel preferences. Complete these steps:

> 1. Filter the Pandas DataFrame based on user inputs for a minimum and maximum temperature.
> 2. Create a heatmap for the new DataFrame.
> 3. Find a hotel from the cities' coordinates using Google's Maps and Places API, and Search Nearby feature.
> 4. Store the name of the first hotel in the DataFrame.
> 5. Add pop-up markers to the heatmap that display information about the city, current maximum temperature, and a hotel in the city.

### Challenge Plan Outline <sup>(instructions as directly from Mod 6 Challenge)</sup>
As for the Basic Project Plan, Challenge deliverables have three components as follows:
<dl>
  <dt>.C1. Retrieve Weather Data</dt>

<dd>Generate a set of 2,000 random latitudes and longitudes, retrieve the nearest city, and perform an API call with the OpenWeatherMap. In addition to the city weather data you gathered in this module, use your API skills to retrieve the current weather description for each city. Then, create a new DataFrame containing the updated weather data.</dd>

  <dt>.C2. Create a Customer Travel Destinations Map</dt>

<dd>Use input statements to retrieve customer weather preferences, then use those preferences to identify potential travel destinations and nearby hotels. Then, show those destinations on a marker layer map with pop-up markers.</dd>

  <dt>.C3. Create a Travel Itinerary Map</dt>

<dd>Use the Google Directions API to create a travel itinerary that shows the route between four cities chosen from the customer’s possible travel destinations. Then, create a marker layer map with a pop-up marker for each city on the itinerary.</dd>
</dl>

### Notes
>- .gitignore
>>Adding config.py necessary to simplify adding adding other files to repository<img src="https://user-images.githubusercontent.com/106628649/178791038-c5eea7cd-67d7-434a-8a19-c4fce5aec9c1.png" width="55%">

>- .csv file
>>Notice regarding line ending characters when uploading files from local computer...

>>  <img src="https://user-images.githubusercontent.com/106628649/178791710-e67ceb4f-f99f-45e4-881b-7f27f36b8c3e.png" width="55%">

>- Randomizing of Latitude and Longitude generation
>> Numpy module np.random.uniform() chosen: satisfies non-integer and number of points requirements, as well as being speedier (100x faster)<sup>(mod 6.1.4)</sup>
>> Other methods considered -- four random module functions: (i) randint(); (ii) random(); (iii) randrange(); uniform()<sup>(random function comparison image below from Mod 6.1.4)</sup>
>>  <img src="https://user-images.githubusercontent.com/106628649/178802063-5e9cc631-0348-444c-bd15-49493224f2c0.png" width="55%">

>- APIs and API keys
>> citipy -- no key required; pip installation required; website: https://github.com/wingchen/citipy

>> OpenWeatherMap -- signed up for generated API key

>> Google Cloud -- API key generated

>> Google Maps, Directions, Places -- API key with attached billing account required

