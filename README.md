# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring climate data and dengue trend in Singapore

### Problem Statement

Dengue is one of the top endemic diseases in Singapore and it has reached new highs in incidence and death rates in recent years [[1]](#1) [[2]](#2). With Singapore having a generally wet and hot climate, and rainfall being one of the main drivers of dengue transmission [[3]](#3) [[4]](#4), this project aims to provide an exploratory analysis on rainfall data and number of dengue cases to improve resource allocation and preventive measures, hence reducing public resource overload.

---

### Datasets

The raw datasets used are in the [`data`](./data/) folder.  
The cleaned datasets used for EDA are in the [`data`](./data/output) folder.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|maximum_rainfall_in_a_day|float|df_month|Highest daily rainfall in each month|
|no_of_rainy_days|float|df_month|Monthly number of rain days|
|total_rainfall|float|df_month|Total monthly rainfall (in mm)|
|wbt_mean|float|df_month|Mean monthly-wet-bulb-temperature (in degree celcius)|
|wbt_min|float|df_month|Mininum monthly-wet-bulb-temperature (in degree celcius)|
|wbt_max|float|df_month|Maximum monthly-wet-bulb-temperature (in degree celcius)|
|mean_rh|float|df_month|Mean relative humidity|
|mean_temp|float|df_month|Mean surface air temperature (in degree celcius)| 
|dengue_cases|float|df_month|Total number of dengue cases in a month|
|---|---|---|---|
|dengue_cases|integer|df_dengue_yearly|Total number of dengue cases in a year|
|---|---|---|---|
|date|datetime64[ns]|cluster_df|date of case recorded|
|street_name|object|cluster_df|street at which the case was reported|
|dengue_cases|object|cluster_df|number of dengue cases|
|latitude|float|cluster_df|latitude of location|
|longitude|float|cluster_df|longitude of location|


---
### Summary of Analysis

A yearly and monthly analysis of the rainfall and dengue data was done. 

The monthly trends of number of rainy days and dengue cases are rather consistent over the years respectively. By comparing the two, dengue data shows a 2-months lagged period of the dengue cases from the number of rainy days. 

There is no apparent correlation between the yearly trends - the peaks in dengue cases finds a corresponding peak in number of rainy days data, but this was not the case anymore for the past 10 years. This could be attributed to the Covid-19 situation, where it induced a spike in dengue cases initially due to more people staying at home and hence being exposed to breeding grounds, and a further surge in Covid-19 cases resulted in lack of detection and reporting of dengue cases which may have been impacted by reduced access to health facilities, and a hesitancy to seek medical care at facilities due to concern of possible exposure to COVID-19 patients.

A cluster analysis was attempted at 3 regions to analyse the effectiveness of Project Wolbachia on dengue prevention. However, further work has to be done to anlayse the impact of number of rainy days on dengue cases. 

--- 
### Conclusions/Recommendations
Based on the analysis, one recommendation will be to make use of the monthly rainfall forecast to optimise prevention strategy and medical resources, especially when preparing for spikes in dengue cases 2 months after a high number of daily rainfall. Besides that, historical dengue data could be shared openly since monthly data after 2019 are unable to be found. Lastly, Project Wolbachia can be accelerated at regions that are more prone to rainfall, which is also a future work for me to work on.


## References

<a id="1">[1]</a> 
National Medical Research Council (NMRC). (n.d.). Integrated Dengue Surveillance in Singapore. Retrieved from https://www.nmrc.gov.sg/docs/default-source/about-us-library/idtf-summary-report.pdf

<a id="2">[2]</a> 
 Chong, K. (n.d.). Singapore records 19 dengue deaths in 2022, nearly four times 2021's toll. The Straits Times. Retrieved from https://www.straitstimes.com/singapore/health/singapore-records-19-dengue-deaths-in-2022-nearly-four-times-2021-s-toll
 
<a id="3">[3]</a> 
Met Office. (n.d.). Singapore Holiday Weather Guide. Retrieved from https://www.metoffice.gov.uk/weather/travel/holiday-weather/asia/singapore

<a id="4">[4]</a> 
Ng, L. C., et. al (2018). IL-1β, IL-6, and RANTES as biomarkers of Chikungunya severity. PLOS Neglected Tropical Diseases, 12(5), e0006935. https://doi.org/10.1371/journal.pntd.0006935

