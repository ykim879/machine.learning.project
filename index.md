
### Introduction/Background 

Transportation emissions are the biggest factor that keep developed countries from matching the sustainability and pollution goals described in the Paris Agreement. It is currently responsible for 28% of all carbon dioxide emissions in the United States and has seen an incredible expansion in the last 30 years, especially in metropolitan cities, like Atlanta, that have seen an 84% overall increase in CO2 emissions. To curtail the rising trend, the Environmental Protection Agency annually imposes a lower CO2 emission limit, forcing companies to invest millions of dollars to make vehicle engines more fuel efficient. This said, some car manufacturers, like Volkswagen, have seen emission increases due to a “large shift towards sport utility vehicles commonly referred to as SUVs” and an overall sale increase throughout the years [3]. This has also been attributed to low gas prices, and this increase in low gas mileage vehicle sales is attributed to the subsequent increase in CO2 transportation emissions [2]. To decrease pollution levels and match the EPA’s emission limit, several companies are investing in electric (EV) and hybrid electric vehicles (HEV). With a rising electric vehicle popularity, there is an expected negative correlation between electric vehicle sales and CO2 transportation emissions.   

### Problem Definition

To help determine the role EV sales has in curtailing CO2 emissions, this project will attempt to develop a correlation between yearly electric vehicle sales and CO2 transportation emissions to predict CO2 emissions based on future EV sales. Due to increasing sales of other gas-powered vehicles, the direct relationship between current EV sales on transportation CO2 emissions is still unknown. Analogously, there is no model predicting future CO2 emissions based off the increasing trend of EV sales relative to non-EV sales. This project will aim to create one by creating regression models mapping CO2 emissions to corresponding EV sales and non-EV sales of the same year. Similarly, there will be an attempt to predict the increase in the volume of future sales based on past sale trends and identify whether there is an increase of EV sales when compared against the sales of internal combustion engine vehicles. Lastly, a clustering analysis will be performed to determine high, medium, and low risk states according to their CO2 emissions history. This will identify states to focus promoting efforts towards to increase EV sales.

### Data Collection
To develop models relating EV sales to transportation CO2 emissions, datasets were collected that detailed the yearly recorded measurements of transportation CO2 levels as well as vehicle sales - EV and non-EV sales - for each state within the United States. The CO2 emissions dataset was referenced from data.gov to ensure the collection of accurate government-sponsored data about the CO2 emissions in the United States. CO2 emissions were measured by million metric tons (Mt). External websites such as Auto Alliance were used to collect EV and non-EV sales data for each state, where sales are measured by number of vehicles. 

The datasets detailing vehicles sales and transportation CO2 emissions were cleaned for corresponding clustering and regression models. Specifically, data corresponding to the time period of 2011 to 2018 was extracted due to that being the recorded starting period of EV sales due to the short history of modern electrical vehicles. For subsequent clustering, the CO2 emissions data was further cleaned to include 2 features with each state being a datapoint: 1) transportation CO2 emissions during 2018 2) net change in transportation CO2 emissions from 2011-2018. These features were chosen because they detail the current state and trends of emissions for each state. Therefore, states can be clustered into risk categories by current emissions and future paths. For regression models, the data for each state was summed to generate total, nationwide EV sales, non-EV sales, and CO2 emissions. These 3 features were chosen to create a multivariate linear regression model relating CO2 emissions to both EV sales and non-EV sales. This is due to the amount sales of non-EV vehicles also impacting CO2 emissions as aforementioned. In addition, the temporal dataset of total, nationwide transportation CO2 emissions and EV sales will be used to create additional regression models for prediction of future CO2 emissions and EV sales. 

![C02 Emissions and Vehicle Sales Table](/images/Picture1.png)


### Methods

For this project, we will be analyzing two types of datasets for each US state: 1) yearly CO2 emission levels 2) yearly EV sales. We will then perform a comparative analysis between the CO2 levels for a calendar year and the corresponding EV sales. We will also perform a regression analysis on the data and use it to predict CO2 levels and EV sales for future years. This is to determine whether increase in EV sales really correspond to decreases in CO2 levels. We will also be using clustering analysis to designate states into emission level categories (e.g. high vs low) and mark the states with high emissions as potential areas to promote EV sales.  

### Potential Results

This project is relating EV sales to transportation CO2 emissions, so potential results include predictions of future EV sales and their subsequent CO2 emissions for future years. This predictive model will be used for specific states within the United States. In addition, another result could be another predictive model that predicts the number of EVs sold for each future year when given a desired CO2 emission for a future date. Another result would be the grouping of states based on their transportation CO2 emissions and EV sales, which will ultimately highlight target regions for improving green transportation. Ultimately, these results will help map out the future role EVs need to play in the fight to curtail CO2 emissions.

### Discussion

For this project, we are trying to predict future yearly EV sales and subsequent CO2 emissions for individual US states. Therefore, a regression analysis will be performed on yearly transportation CO2 emissions and electric vehicle sales over the past 10 years, which brings forth a potential problem: Increasing EV sales may not correlate to decreasing transportation CO2 emissions, because EV sales are largely residential while commercial vehicles (trucks, buses, etc.) also play a big role in CO2 emissions. To help solve this, we may use current EV sales trends to predict the future sales of upcoming commercial EVs, such as Tesla’s Cybertruck, and their subsequent emissions impact. In addition, EV sales do not have a long history with recorded sales starting in 2010, so future predictions will only rely on yearly trends over 10 years.

### References

[1] “Sources of Greenhouse Gas Emissions,” EPA, 09-Sep-2020. [Online]. Available: https://www.epa.gov/ghgemissions/sources-greenhouse-gas-emissions#transportation.  [Accessed: 01-Oct-2020].
  
[2] N. Popovich and D. Lu, “The Most Detailed Map of Auto Emissions in America,” The New York Times, 10-Oct-2019. [Online]. Available: https://www.nytimes.com/interactive/2019/10/10/climate/driving-emissions-map.html.  [Accessed: 01-Oct-2020].  

[3] Office of Transportation and Air Quality, A. Hula, R. French, A. Maguire, A. Bunker, and T. Rojeck, Environmental Protection Agency, 2020. Available: https://nepis.epa.gov/Exe/ZyPDF.cgi?Dockey=P100YVFS.pdf

### Potential Datasets

[1] Transportion energy-related carbon dioxide emissions, https://www.eia.gov/environment/emissions/state/excel/transportation.xlsx  

[2] DARTE Annual On-road CO2 Emissions on a 1-km Grid, Conterminous USA, V2, 1980-2017, https://daac.ornl.gov/cgi-bin/dsviewer.pl?ds_id=1735 

[3] U.S. Light-Duty Advanced Technology Vehicle (ATV) Sales* (2011–2019), https://autoalliance.org/energy-environment/advanced-technology-vehicle-sales-dashboard/ 

[4] State EV Registration Data, https://www.atlasevhub.com/materials/state-ev-registration-data/ 

[5] Monthly Plug-In EV Sales Scorecard: Historical Charts, https://insideevs.com/news/344007/monthly-plug-in-ev-sales-scorecard-historical-charts/ 
