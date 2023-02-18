
<h1 align="center"> An Analysis of Singapore’s Weather Conditions for </br> 
the Singapore Tourism Board’s Infographic </h1>
<h3 align="center"> DSIF 9 Project 1 </h3>  

</br>


![image alt ><](https://cdn.dribbble.com/users/28455/screenshots/1389791/media/c5abb9d81320af5cedd449fdbc8d5408.gif)


<!-- CONTENTS -->
<h2 id="table-of-contents"> Contents</h2>

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#background"> ➤ Background</a></li>
    <li><a href="#problem-statement"> ➤ Problem Statement</a></li>
    <li><a href="#external-research"> ➤ External Research and Additional References</a></li>
    <li><a href="#data-dictionary"> ➤ Data Dictionary</a></li>
    <li><a href="#analysis"> ➤ Analysis Approach</a></li>
    <li><a href="#recommendations"> ➤ Findings and Recommendations</a></li>
    <li><a href="#credits"> ➤ Credits </a></li>
  </ol>
</details>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- BACKGROUND -->
<h2 id="background"> Background </h2>

<p align="justify"> 
    
According to the [Meteorological Service Singapore](http://www.weather.gov.sg/climate-climate-of-singapore/#:~:text=Singapore%20is%20situated%20near%20the,month%2Dto%2Dmonth%20variation), Singapore has typical tropical climate with adundant rainfall, high and uniform temperatures and high humidity all year round, since its situated near the equator. There are many factors that help us understand the climate of a country and in this project we are going to look into a few, especially rainfall.

Singapore’s climate is characterized by two main monsoon seasons separated by inter-monsoonal periods.  The **Northeast Monsoon** occurs from December to early March, and the **Southwest Monsoon** from June to September.

The major weather systems affecting Singapore that can lead to heavy rainfall are:

<ul>
<li>Monsoon surges, or strong wind episodes in the Northeast Monsoon flow bringing about major rainfall events;</li>
    
<li>Sumatra squalls, an organised line of thunderstorms travelling eastward across Singapore, having developed over the island of Sumatra or Straits of Malacca west of us;</li>
    
<li>Afternoon and evening thunderstorms caused by strong surface heating and by the sea breeze circulation that develops in the afternoon.</li>
</ul> 

Singapore’s climate station has been located at several different sites in the past 140 years. The station had been decommissioned at various points in the past due to changes to local land use in the site’s vicinity, and had to be relocated. Since 1984, the climate station has been located at **Changi**.

There are other metrics of climate such as temperature, humidity, sunshine duration, wind speed, cloud cover etc. All the datasets used in the project come from [data.gov.sg](data.gov.sg), as recorded at the Changi climate station.
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="problem-statement"> Problem Statement</h2>

<p align="justify"> 
As part of their website revamp, the Singapore Tourism Board (STB) is looking to create an online infographic guide for tourists who are interested in outdoor activities. <br> 

Singapore’s weather is known to be humid, with either sunny or rainy days (occasionally both). Given recent weather fluctuations arising from climate change and dense urban infrastructure, the STB Marketing team wants to adopt a data-driven approach to craft its marketing message for people who are new to Singapore. <br>
    
They have engaged us, the Data Analytics team, to help provide information that would feed into a guide. The information should shed light on Singapore's general weather patterns throughout the year, which time of the year is best to visit, weather conditions tourists should look out for so they can plan their itinerary and attire, and whether there are any precautions that should be taken. <br>

Questions the Data Analytics team hopes to answer, in order to inform the Marketing team's publicity materials:
<ol>    
    <li> Since the 1980s to today, has Singapore gotten warmer and rainier? </li>
    <li> Which months are best for outdoor activities? </li>
    <li> What do the findings mean for tourists looking for a fun day out in Singapore? </li>
</ol>

</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="external-research"> External Research and Additional References</h2>

<p align="justify"> 

Being a dense concrete jungle, Singapore experiences warming faster than the global average because of the urban heat island effect - a phenomenon of urban structures trapping heat in the day and releasing it at night. During the inter-monsoon season in April and May 2022, temperatures in Singapore hit record highs. Temperatures of 36.8 degrees Celsius were recorded at Admiralty on April 1, which is 0.2 degrees below the all-time high of 37 degrees Celsius. 

People in Singapore must get used to higher air temperatures due to global warming and urbanisation, which produces additional local warming. This heat is expected to intensify within the next five years as the world faces a nearly 50 per cent chance of briefly reaching 1.5 deg C above pre-industrial levels.

To avoid heat-related stress, lethargy, light-headedness, cramps and heat rash, it is recommended that people wear loose, breathable clothing, and hats to protect from direct sunlight. Drinking plenty of water throughout the day, taking periodic breaks in the shade and portable fans can be helpful.  

News sources referenced: [Straits Times, 13 May 2022](https://www.straitstimes.com/singapore/environment/hottest-temperature-since-1983-recorded-in-spore-during-recent-weeks-of-warm-weather) and [ChannelNewsAsia, 4 Jun 2022](https://www.channelnewsasia.com/singapore/hot-weather-high-temperature-singapore-climate-change-health-2722321).


</p>



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="data-dictionary"> Data Dictionary</h2>

Additional datasets were referenced from Data.gov.sg. The details of each dataset are outlined in the data dictionary below.

### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|total_rainfall|float|[rainfall-monthly-total](https://data.gov.sg/dataset/rainfall-monthly-total)|Total rainfall in mm from January 1, 1982 to August 31, 2022. A day is considered to have “rained” if the total rainfall for that day is 0.2mm or more.| 
|no_of_rainy_days|integer|[rainfall-monthly-number-of-rain-days](https://data.gov.sg/dataset/rainfall-monthly-number-of-rain-days)|Number of rain days in the month from January 1, 1982 to August 31, 2022.| 
|humidity|float|[relative-humidity-monthly-mean](https://data.gov.sg/dataset/relative-humidity-monthly-mean)|Mean relative humidity in percentage from January 1, 1982 to October 31, 2022. This refers to the amount of water vapour present in air expressed as a percentage of the amount needed for saturation at the same temperature.| 
|sunshine|float|[sunshine-duration-monthly-mean-daily-duration](https://data.gov.sg/dataset/sunshine-duration-monthly-mean-daily-duration)|Mean sunshine hours in a day from January 1, 1982 to October 31, 2022. Sunshine duration is directly affected by the amount of cloud cover present.| 
|surface_temp|float|[surface-air-temperature-monthly-mean](https://data.gov.sg/dataset/surface-air-temperature-monthly-mean)|Mean air temperature in degree Celsius from January 1, 1982 to October 31, 2022.|
|wet_bulb_temperature|float|[wet-bulb-temperature-hourly](https://data.gov.sg/dataset/wet-bulb-temperature-hourly)|Hourly wet bulb temperature in degree Celsius from January 1, 1982 to October 31, 2022.|
|region|string|[visitor-international-arrivals-to-singapore-by-country-monthly](https://data.gov.sg/dataset/total-visitor-international-arrivals-to-singapore?resource_id=83063203-ff81-4764-a9dc-c4e209921fe7)|Region of origin for visitors to Singapore from 1 Jan, 1978 to 30 November, 2015|
|country|string|[visitor-international-arrivals-to-singapore-by-country-monthly](https://data.gov.sg/dataset/total-visitor-international-arrivals-to-singapore?resource_id=83063203-ff81-4764-a9dc-c4e209921fe7)|Country of origin for visitors to Singapore from 1 Jan, 1978 to 30 November, 2015|
|no_of_visitor_arrivals|integer|[visitor-international-arrivals-to-singapore-by-country-monthly](https://data.gov.sg/dataset/total-visitor-international-arrivals-to-singapore?resource_id=83063203-ff81-4764-a9dc-c4e209921fe7)|Number of visitor arrivals to Singapore from 1 Jan, 1978 to 30 November, 2015|
|month|integer|available in all datasets|Month of data collection for each variable in the dataset.| 



![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="analysis"> Analysis Approach </h2>

The steps taken to analyse the datasets were as follows:

<ol>    
    <li> Imported the data for inspection and checked for missing values, unexpected outliers, duplicates or clearly erroneous data points. </li>
    <li> Converted data that was inconsistent with the other data sets to prepare it for merging and further analysis by making sure the columns to be merged on are at the same granularity (i.e., in year and month instead of hours). </li>
    <li> Fixed incorrect data types, including type casting date values into Datetime. </li>
    <li> Visualised the data to better understand each variable, and the relationships between them.  </li>
    <li> Interpreted the plots to develop recommendations and address the problem statements. </li> 
</ol>


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2 id="recommendations"> Findings and Recommendations </h2>

<ol>
<li>Since the 1980s to today, has Singapore gotten warmer and rainier?</li>
    <ul>
        <li>Singapore has gotten warmer over the last four decades. Surface temperature has increased between 1982 to 2022, particularly in the months of April to July, and November to December. Given that our temperatures are likely to continue increasing (see section on external references for news articles), we need to educate people in Singapore and visiting tourists on the dangers of spending excessive time outdoors in the summer months where the surface temperatures are at their highest. </li>
        <li>Even though the mean annual rainfall has not changed substantially in the last 40 years, Singapore is experiencing higher rainfall in certain months - specifically at the end of the year in the months of November to January, coinciding with the Northeast monsoon period. The higher intensity of rainfall brings with it increased threats of flooding, accidents, or traffic incidents.</li>
    </ul>

<li>Which months are best for outdoor activities?</li> 
    <ul>
        <li>The best months for outdoor activities are likely to be February to March, or August to October.</li>
        <li>These months are less likely to see very sunny or rainy days. The wet-bulb temperature is not at its highest so even if a person gets prolonged exposure to the heat or sun, their sweat can still easily evaporate and they can cool off in the outdoors.</li>
    </ul>
    
<li>What does this mean for tourists looking for a fun day out in Singapore?</li> 
    <ul>
        <li>The effect of humidity on outdoor activities is constantly palpable in Singapore, where the average levels of humidity have remained high in recent years at around 80-85%.</li>
        <li>Try to time their trips in the months of February-March or August-October to avoid extremely warm temperatures or wet weather. Bring along light, airy clothes made of material such as cotten or linen, and also consider packing shorts and bringing along a hat or cap to shield against the sun. Suncreen is also strongly advised.</li>
        <li>If they're travelling during the months of April-July, practice additional precautions such as frequently hydrating, not engaging in too strenuous outdoor activities, and taking regular breaks in the shade. </li>
        <li>If they're travelling during the months of November-January, pack umbrellas, ponchos, waterproof or rubber shoes, or be prepared to have flexible plans and spend most of their time in Singapore's ubiquitous shopping malls. </li>
    </ul>
    
<li>Additional recommendations for visitors from specific countries</li> 
    <ul>
        <li>The top countries of origin for international visitors between 2010 and the latest year of available data 2017 are Indonesia, China, Malaysia, Australia and India.</li>
        <li>Visitors from Southeast Asian countries are likely to be familiar with Singapore's weather patterns, given their geographic proximity, similar climate conditions, and exposure to monsoon rains.</li>
        <li>Visitors from China are most likely to visit in Feb, Jul and Aug. Visitors from Australia are likely to visit in Jan, Jul and Sep. Visitors from India are most likely to visit between Apr to Jun.  </li>
        <li>For visitors from China, Australia, and India, the Marketing Team may want to take note of the months that they're most likely to visit and tailor specific recommendations on what to pack, activities to do, and attractions to see. The Marketing team could design a customised email journey for visitors from these specific countries with a link to the infographic on the new website, timing the emails to be sent right before those months of peak visitorship. This improves relevance to the tourists and drives web traffic to the new site.  </li>
    </ul>
    
<p align="center"> 
</p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<!-- CREDITS -->
<h2 id="credits"> Credits</h2>

Referenced ReadMe file from [Mohammad Amin Shamshiri](https://github.com/ma-shamshiri/Pacman-Game/blob/master/README.md)

Acknowledgements: Based on UC Berkeley's Pacman AI project, <a href="http://ai.berkeley.edu">http://ai.berkeley.edu</a>
