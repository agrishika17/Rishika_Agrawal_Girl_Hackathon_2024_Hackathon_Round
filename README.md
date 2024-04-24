# Rishika_Agrawal_Girl_hackathon_Ideathon_Round

## Problem Statement
In the face of growing environmental challenges, there is a pressing need to leverage AI technologies to monitor, analyze, and mitigate environmental issues. By harnessing the power of AI, we can gain valuable insights into environmental data, predict and prevent natural disasters, and promote sustainable practices. This will enable us to make informed decisions and take proactive measures to protect our planet for future generations. The evolution of AI has been nothing short of extraordinary. From humble beginnings, machines now learn, adapt, and even create with startling sophistication.  This power can be used to address the challenges we face. 

Problem Statement: The objective is to create an AI-based system that focuses on essential aspects of environmental conservation. The system should be able to monitor and analyze environmental data, predict and prevent natural disasters, and promote sustainable practices.
* Disaster Relief: Enhance disaster relief and response efforts by leveraging satellite imagery during disasters like floods and wildfires, integrating existing geospatial information, and utilizing environmental data for affected regions.

## Solution
Development of an AI model which takes environmental variables of the past ten years and based on that data gives the prediction of one or more dominant factors which can be the primary cause of the natural disaster and then compares those factors against a threshold to determine which areas can be most affected by the disaster. Since the model takes into account data of multiple years in advance, it can be used to predict a disaster well before it happens and aid in the evacuation efforts. Along with the environmental factors of a particular place (example elevation for flood, seismic zone for earthquake), socio economic factors such as area’s population density, and area distribution based on other factors(for example distribution based on wealth, divide of rural vs urban) can be used to determine which areas will be most critically hit and will affect how much population. This can help in evacuation efforts. Additionally predictive data of months of a year can be used to judge the seasonality of the disaster, i.e, prediction of whether the disaster is likely to happen that particular year or not based on the established seasonality of disaster in the preceding years.
### Wildfire prediction model
Wildfire prediction model can be explained by taking the example of a city in Kerala -> Kozhikode
A heavy rainfall can be defined as rainfall greater than 100 mm in 24 hours. If a lot of rainfall is received in an area with low elevation such as Kozhikode (1 m - 50 m approx) that can potentially lead to flooding if the drainage system is not adequate. Rainfall depends on other environmental factors such as humidity, max. temperature, dew, cloud cover, visibility, sea level pressure, wind direction, wind speed to name a few. By taking into account the data of previous (7 days) (3 days in implementation) a prediction for the rainfall that can occur after 7 days can be made. This can give an idea about whether flooding is possible in the region or not (if it is greater than a threshold then flooding is possible). After the rainfall prediction, by using the data from the elevation of different areas of the district, it is possible to evaluate which areas are at risk of flooding. Furthermore using the socio economic distribution data (population density, rural vs urban areas, slums etc.) the impact can be measured on that area & hence proper arrangements can be made.

## Setup of local environment
1. Fork this repository.
2. Run the command `git clone https://github.com/agrishika17/Rishika_Agrawal_Girl_Hackathon_2024_Ideathon_Round.git`
3. The dataset for training and testing the models (wildfire prediction) is in the folder "datasets".
4. To run the .ipynb files, user need to have Anaconda Navigator installed in the local system to access the Jupyter Notebook.
5. Run the jupyter notebook `fetch_imd_data.ipynb` in "code" folder to download the dataset of the precipitation/rainfall and temperature (as tmax and tmin) for the last 10 years of India region. (Don't forget to install imblib. For this run `pip install imdlib` in the jupyter notebook environment).
6. The satellite images used in the NDVI calculation is imported from the "LANDSAT 8 Collection 2 Tier 2" collection via Google Earth Engine. These images can also be downloaded from the Earth Explorer.
7. To calculate NDVI (Normalized difference vegetation index), navigate to `calculate_ndvi.ipynb` file. 
[Formula to calculate NDVI = (BAND5-BAND4)/(BAND5+BAND4) , where Band 5 is for Near-Infrared spectroscopy and Band4 is for Red spectroscopy.]
8. The file `calculate_ndvi.ipynb`is written in Google Earth Engine code editer. To run this file navigate to the google earth engine site `https://code.earthengine.google.com/5000efc78790babe8974970ac65a82a6`, provide authenticatation and then run the code file. 
9. Mean NDVI value can be inspected for each pixel of the images displayed via Inspector section on the right side of the code editor. 
10. For LST(Land Surface Temperature) calculation, a thorough block diagram is attached in jpg format which shows how an Landsat8 image can be used to calculate NDVI and LST.

## Demo
