# Rishika_Agrawal_Girl_hackathon_Ideathon_Round

## Problem Statement
In the face of growing environmental challenges, there is a pressing need to leverage AI technologies to monitor, analyze, and mitigate environmental issues. By harnessing the power of AI, we can gain valuable insights into environmental data, predict and prevent natural disasters, and promote sustainable practices. This will enable us to make informed decisions and take proactive measures to protect our planet for future generations. The evolution of AI has been nothing short of extraordinary. From humble beginnings, machines now learn, adapt, and even create with startling sophistication.  This power can be used to address the challenges we face. 

Problem Statement: The objective is to create an AI-based system that focuses on essential aspects of environmental conservation. The system should be able to monitor and analyze environmental data, predict and prevent natural disasters, and promote sustainable practices.
* Disaster Relief: Enhance disaster relief and response efforts by leveraging satellite imagery during disasters like floods and wildfires, integrating existing geospatial information, and utilizing environmental data for affected regions.

## Solution

Development of an AI model for wildfire prediction which utilizes environmental data from the preceding ten years to identify one or more dominant factors that contribute to the likelihood of a wildfire outbreak. The model compares the identified factors against predetermined thresholds to predict which areas are most susceptible to wildfire damage. Because the model incorporates multiple years of data, it can accurately predict potential disasters well in advance, which is valuable information for evacuation efforts.

In addition to environmental factors such as elevation and surface temperature, the model also considers socio-economic factors such as population density and area distribution based on wealth or urbanization. This information is used to determine which areas are most at risk and likely to affect the largest populations. Consequently, these insights can help optimize evacuation efforts and minimize damage.

Furthermore, the model can analyze predictive data from previous years to determine the seasonality of a potential disaster. This information can be used to determine whether an area is likely to face a wildfire outbreak during a particular season based on its historical patterns. Such insights can help prepare for the potential disaster and take preventive measures.

### Predictive Model for Damage Reduction and Response Optimization during wildfire

![Alt text](https://drive.google.com/file/d/1BbCOCXdyZbhKtfQgn1jcedfAxKhsZKGb/view?usp=sharing)

![Alt text](https://drive.google.com/file/d/1btA4AUwcqgWUbUo7UXjSwDncJ7_HLgGn/view?usp=sharing)

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
10. For LST(Land Surface Temperature) calculation, a thorough block diagram is attached in jpg format [navigate to `code/lst/L8_to_LST.jpg`] which shows how an Landsat8 image can be used to calculate NDVI and LST.
11. Navigate to `flowcharts` to get thorough insights on how the model utilizes all the parameters and data collected and process involved to efficiently predict the wildfire.

