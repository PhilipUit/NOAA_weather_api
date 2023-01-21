# NOAA_weather_api
We will be working with NOAAs weather API. This API will allow you to retrieve a variety of data from a specific weather station(s), of your choice.

### API Documentation: https://www.ncdc.noaa.gov/cdo-web/webservices/v2#gettingStarted

### As the API documentation page states, you will need to register for your own credentials. Following the instructions at https://www.ncdc.noaa.gov/cdo-web/token to register.
Now we need to determine a weather station that we would like to retrieve our data for. Use the following link to get the id for a NOAA weather station. https://www.ncdc.noaa.gov/cdo-web/datatools/findstation"

Requirements:
Using the NOAA API, retrieve data for a weather station of your choice. Based on the station you pick,

Determine an appropriate dataset:
I choose to use a dataset that is relevant to me. This dataset station ID & info is from the website: https://www.ncdc.noaa.gov/cdo-web/datatools/findstation.

I choose to use data from a local Colorado station (station id:GHCND:USC00055402) that is a collection of Max daily temperatures. (TMAX) Since we need 3 years of data, I pulled daily data from years 2016 - 2018.

#### Setup/Intro:
Determine an appropriate dataset/Determine an appropriate dataset type -
Before starting, we need to make sure that we have an appropriate dataset. We will use data found from a local Lakewood, CO station. We will look at MAX daily temperature data, which is relevant to the the average dataset outlined in the demo, is similar in structure, and is appropriate to work on in this assignment as it is different but similar, intersting to me personally, and also will pull from 3 years of data as outlined spanning from years 2016-2018 found here:https://www.ncdc.noaa.gov/cdo-web/webservices/v2#dataTypes. Since we can only pull 1 year of data at a time, we will pull all 3 years seperately and then will combine them into one master dataframe before we put into a csv to finalize the assignment later on.

The dataset type we will be using is MAX daily Temp. from a local NOAA station from years 2016-2018. Again, before starting -- we will need to make sure that we will be able to work on the data once we pull it into a dataframe, or something similar. After investigation, it is determined that this data is in JSON format that we can easily convert to dict, or dictionary format later on. We will use the json.loads(r.text) function with datatypes_dict.keys() function to pull the data in. We will then use the pd.DataFrame() function later on, as we will demonstrate to convert the dict to a dataframe. Now that we know the dataset type, and that we can work with it, as well as knowing that the data is appropriate, we will more forward and will outline our steps/processes as we go.
