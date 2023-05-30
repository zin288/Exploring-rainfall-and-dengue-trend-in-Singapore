# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 1: Exploring climate data and dengue cases in Singapore

### Problem Statement

Dengue fever has been a significant public health concern in Singapore, impacting the population's health and well-being. The country has experienced periodic outbreaks of dengue fever, with varying intensities and geographical spread. The disease is transmitted by the Aedes mosquito and can lead to severe symptoms, hospitalizations, and, in some cases, fatalities. Analyzing the trends of dengue fever cases is of utmost importance as it provides valuable insights into the patterns and dynamics of the disease. Understanding the factors that contribute to the spread of dengue, including rainfall patterns, enables health authorities to implement targeted prevention and control measures. By analyzing the trends, authorities can better allocate resources, enhance mosquito control efforts, and educate the public about effective preventive measures. This analysis plays a crucial role in mitigating the impact of dengue fever on the Singapore population and improving overall public health outcomes.

---

### Datasets

The raw datasets used are in the [`data`](./data/) folder.  
The cleaned datasets used for EDA are in the [`data`](./data/output) folder.

|Feature|Type|Dataset|Description|
|---|---|---|---|
|maximum_rainfall_in_a_day|float|df_month|Highest daily rainfall in each month|
|no_of_rainy_days|float|df_month|Monthly number of rain days|
|total_rainfall|float|df_month|Total monthly rainfall in mm|
|wbt_mean|float|df_month|Mean monthly-wet-bulb-temperature|
|wbt_min|float|df_month|Mininum monthly-wet-bulb-temperature|
|wbt_max|float|df_month|Maximum monthly-wet-bulb-temperature|
|mean_rh|float|df_month|Mean relative humidity|
|mean_temp|float|df_month|Mean surface air temperature| 
|dengue_cases|float|df_month|Total number of dengue cases in a month|

---
### Summary of Analysis

A yearly and monthly analysis of the rainfall and dengue data was done. 

The monthly trends of number of rainy days and dengue cases are rather consistent over the years respectively. By comparing the two, dengue data shows a 2-months lagged period of the dengue cases from the number of rainy days. 

There is no apparent correlation between the yearly trends - the peaks in dengue cases finds a corresponding peak in number of rainy days data, but this was not the case anymore for the past 10 years. This could be attributed to the Covid-19 situation, where it induced a spike in dengue cases initially due to more people staying at home and hence being exposed to breeding grounds, and a further surge in Covid-19 cases resulted in lack of detection and reporting of dengue cases which may have been impacted by reduced access to health facilities, and a hesitancy to seek medical care at facilities due to concern of possible exposure to COVID-19 patients.

A cluster analysis was attempted at 3 regions to analyse the effectiveness of Project Wolbachia on dengue prevention. However, further work has to be done to anlayse the impact of number of rainy days on dengue cases. 

--- 
### Conclusions/Recommendations
Based on the analysis, one recommendation will be to make use of the monthly rainfall forecast to optimise prevention strategy and medical resources, especially when preparing for spikes in dengue cases 2 months after a high number of daily rainfall. Besides that, historical dengue data could be shared openly since monthly data after 2019 are unable to be found. Lastly, Project Wolbachia can be accelerated at regions that are more prone to rainfall, which is also a future work for me to work on.