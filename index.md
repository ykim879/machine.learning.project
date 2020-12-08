
### Introduction/Background 

Transportation emissions are the biggest factor that keep developed countries from matching the sustainability and pollution goals described in the Paris Agreement. It is currently responsible for 28% of all carbon dioxide emissions in the United States and has seen an incredible expansion in the last 30 years, especially in metropolitan cities, like Atlanta, that have seen an 84% overall increase in CO2 emissions. To curtail the rising trend, the Environmental Protection Agency annually imposes a lower CO2 emission limit, forcing companies to invest millions of dollars to make vehicle engines more fuel efficient. This said, some car manufacturers, like Volkswagen, have seen emission increases due to a “large shift towards sport utility vehicles commonly referred to as SUVs” and an overall sale increase throughout the years [3]. This has also been attributed to low gas prices, and this increase in low gas mileage vehicle sales is attributed to the subsequent increase in CO2 transportation emissions [2]. To decrease pollution levels and match the EPA’s emission limit, several companies are investing in advanced technology vehicles (ATVs) such as electric (EV), plug-in hybrid electric vehicles (PHEV) and hybrid electric vehicles (HEV). With a rising electric vehicle popularity, there is an expected negative correlation between electric vehicle sales and CO2 transportation emissions.   

### Problem Definition
To understand the role ATVs have in curtailing CO2 emissions, this project will attempt to determine the impact of ATV sales on nationwide efforts to mitigate transportation CO2 emissions through various methods. Due to increasing sales of other gas-powered vehicles, the direct relationship between current EV sales on transportation CO2 emissions is still unknown. Similarly, there is no current model determining whether using electric vehicles is a best way to mitigate CO2 emission. Therefore, this project will attempt to analyze the impact of electric vehicles on CO2 emissions by creating a regression model mapping CO2 emission levels to EV sales and non-EV sales of the same year. This will be extended to regression models that will attempt to map the time history of CO2 emissions for the USA and its two highest-emitting states to predict future trends in transportation CO2 emissions. References also hint at gas prices affecting the sales of CO2 emitting vehicles, so this project will also attempt to bring to light this claim by determining the relationship between gas prices and CO2 emissions. In addition, the weight of current emission mitigation efforts by state governments have not been assessed, so this project will also determine the weight of ATV sales as well as other eco-friendly activities in these mitigation efforts. Finally, while the time history of CO2 emissions and ATV sales exist for each state, they have not been used collectively to assess each state's risk to future high transportation CO2 emissions. This project aims to do so to each US state to determine what states would benefit the most from an increase in the ratio of ATVs to internal combustion engine vehicle sales.

### Data Collection

To develop models relating EV sales to transportation CO2 emissions, datasets were collected that detailed the yearly recorded measurements of transportation CO2 levels as well as ATV sales for each state within the United States. The CO2 emissions dataset was referenced from data.gov to ensure the collection of accurate government-sponsored data about the CO2 emissions in the United States. CO2 emissions were measured by million metric tons (mmt). External websites such as Auto Alliance were used to collect data for EV, HEV, and PHEV for each state, where sales are measured by number of vehicles. Additionally total vehicle registrations for each state in 2018 was also collected as well as a time history of total vehicle sales nationwide.

The datasets detailing vehicles sales and transportation CO2 emissions were cleaned for corresponding clustering and regression models. Specifically, data corresponding to the time period of 2011 to 2018 was extracted due to that being the recorded starting period of electric sales due to the short history of modern electrical vehicles. For subsequent clustering, the CO2 emissions data was further cleaned to include 6 features with each state being a datapoint: 1) transportation CO2 emissions during 2018, 2) net change in transportation CO2 emissions from 2011-2018, 3) total vehicle registrations in 2018 4) total vehicle sales from 2011-2018 for EV, HEV, and PHEV. These features were chosen because they detail the current state and trends of emissions for each state. Therefore, states can be clustered into risk categories by current ATV sales, CO2 emissions, and their trends. For regression models, the data for each state was summed to generate total, nationwide ATV sales total, non-EV sales, and CO2 emissions as seen in Table 1. These 3 features were chosen to create a multivariate linear regression model relating CO2 emissions to both EV sales and non-EV sales. This is due to the amount sales of non-EV vehicles also impacting CO2 emissions as aforementioned. In addition, the temporal dataset of total, nationwide transportation CO2 emissions and EV sales will be used to create additional regression models for prediction of future CO2 emissions and EV sales.  

The random_forest_data.xlsx data set combines data for each individual state on the 1) emissions in 2018, 2) the change in emissions from 2011-2018, 3) total registered commercial vehicle in 2018, 4) total EV sales from 2011-2018, 5) total HEV sales from 2011-2018, 6) total PHEV sales from 2011-2018, 7) change alternative fuel stations from 2011-2018, 8) percentage of people driving alone to commute in 2018 and the 9) change of vehicles on the highway is used to categorize the importance of these attributes for emissions mitigation. The combined data uses the ATV information from the Auto Alliance website along with datasets pulled from the bts.gov website. 

The polynomial regression algorithms use datasets on national CO2 emission from 1980-2017, along with the corresponding gas prices from 1997-2017, as well as individual CO2 emission levels and gas prices for the two highest risk states, California and Texas from 1997-2017.  

### Methods

To develop a relationship between yearly electric vehicle sales and CO2 transportation emissions, 10 different types of datasets, described in the data collection section above, were used to carry out 4 different types of analyses. The analysis on ATV started with a risk assessment for each state using K-means clustering with 6 separate features: 1) transportation CO2 emissions during 2018, 2) net change in transportation CO2 emissions from 2011-2018, 3) total vehicle registrations in 2018 4-6) total vehicle sales from 2011-2018 for EV, HEV, and PHEV. A k-means algorithm is used due to risk designation being a hard categorization which deemed this algorithm more effective over other clustering techniques like a gaussian mixture model. The second analysis was a random forest algorithm to determine the feature importance of emission mitigation activities, using the above-mentioned data sets along with additional datasets on the percentage change of alternative fuel stations added, the change in vehicle passing through highways, and the percentage of people commuting by themselves. This algorithm will determine which features hold the biggest impact on emission mitigation 

The following analysis involves a linear regression between CO2 emission and vehicle sales– both EV and non-EV sales. This offered a novel model that can be used to predict future transportation CO2 emissions based off the trends of EV sales relative to non-EV sales. The final analysis consisted of polynomial regression models based of on the nationwide CO2 data, and the data from the two highest risk states where the relationship between gas prices throughout history, and the relationship between gas prices and CO2 emissions is further studied. 

To determine the weight of various emission mitigation factors, a Random Forest model was developed and used to determine the feature importance of the 9 determined features that are related to vehicle usage and transportation. Each US state and the District of Columbia acted as data points and classifications for each state was based on that provided by Climate.gov. Specifically, each state was labeled on an integer scale of 0-4 based on the number of emission mitigation activities promoted by the state [4].  

### Results

As seen in Figure 1, all 50 US states as well as the District of Columbia have been clustered into low, medium, and high-risk categories based on their transportation CO2 emissions relative to each other and their volume of vehicle. High recent CO2 emissions, high increases in CO2 emissions from 2011 to 2018 and a high total amount if vehicle sales indicate high risk. The individual designations of each state can be seen in Table 2. The majority of states (29) are categorized to be low risk while 19 states make up medium risk categories, which includes the state of Georgia. While most medium and low risk states are clustered closely, the high-risk states of California, Florida, and Texas account generate relatively much larger transportation CO2 emissions with Texas additionally experiencing much larger increases from 2011-2018. The changes in emissions in California and Florida are comparable to low-risk and medium-risk states, but experience higher absolute, yearly transportation CO2 emissions.  

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/kmeans_risk_assigment_visualization.png?raw=true">
</p>
<p align="center">
  Figure 1: a) 2D visualization of K-means risk assignment clustering of states b) 3D visualization of K-means risk assignment clustering of states
</p>

<p align="center">
  Table 2: List of US states and risk designation 
</p>

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/kmeans_risk_assigment_table.png?raw=true">
</p>

The Random Forest model was trained and optimized to correctly classify the states based on their emission mitigation activity labels. The model was trained using all 50 states and the number of estimators was optimized for an unlimited depth of the decision trees to achieve an OOB accuracy score of at least 0.95. The number of estimators was determined to be 10, which achieved an average OOB accuracy score of ~0.98. After the Random Forest model was developed, the feature importance of all 9 Random Forest features were determined as shown in Figure 2. The commuting mode, specifically the amount of people driving alone versus carpooling, cycling, walking, etc was the most importance mitigation activity. The promotion of PHEVs and EVs are the next most important mitigation activities. Transportation CO2 emissions and change in emissions are the 3rd and 4th most important features respectively, signaling their importance in the push towards emission mitigation activities. 

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/random_forest_feature_importance.png?raw=true">
</p>

<p align="center">
Figure 2: Feature Importance for Emissions Mitigation
</p>

The relationship between CO2 emissions and vehicle sales, seen in Figure 4, is explored through a multivariate linear regression model using the yearly nationwide changes in transportation emission as well as EV and non-EV sales. Equation [1] shows a positive relationship between transportation CO2 emissions, and EV and non-EV sales, regardless of the fact that EVs do not contribute to the CO2 emission in real life. This model predicts that electrical vehicle sales contribute to 1.55e8 MT of CO2 a year. 

<p align="center">
  Change in CO2 emissions = 1.55e05 (EV Sales) +  7.78e07 (Non−EV Sales) - 9.88e14 [1]
</p>

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/linear_regression_plot.png?raw=true">
</p>

<p align="center">
Figure 3: Linear Regression between CO2 Emissions, EV sales, and Non-EV sales 
</p>

A seven-degree polynomial regression is carried out on the nationwide C02 emission data from 1980 to 2017 and extrapolated until the year 2020 to predict the C02 levels for the following year. Similarly, the same procedure is carried out with an eight-degree polynomial regression for national gas prices and the emission levels, where data is taken from 1980 to 2017 is used to predict the CO2 emission nationwide according to an increase in gas prices. It is interesting to note that the CO2 emission level starts to decrease drastically after the prices surpasses $3 a gallon. 

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/national_polynomial_regression_plots.png?raw=true">
</p>

<p align="center">
Figure 4: Nationwide expected behavior regarding CO2 emission and the predicted emission levels according to nationwide average gas prices.  
</p>

A similar procedure is used for the two highest risk states, Texas, and California, where a seven and nine-degree polynomial regression is carried out for the extrapolation of CO2 emission data from 1980-2017, respectively. It is interesting to note that that while California seems to follow a similar behavioral pattern to the one expected nationwide, where it decreases after 2020, Texas is predicted to continue increasing exponentially, even when it boasts a smaller CO2 emission for the same gas prices. Both Texas and California follow the same behavior for an increase in gas prices, with Texas having an overall lower emission level with respect to the price. This is due to the larger population and non-EV sales found in Texas, where buyers aren't pressed nor incentivized to pay the slightly more expensive EV models due to the diminished returns as a result of the cheaper gas prices. This is evident in the similarity between emission levels, regardless of the gas price and the lack of a clearly decreasing slope until the gas price surpasses $3.25. 

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/cali_polynomial_regression_plots.png?raw=true">
</p>

<p align="center">
Figure 5: California expected behavior regarding CO2 emission and the predicted emission levels according to California average gas prices.  
</p>

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/report_images/texas_polynomial_regression_plots.png?raw=true">
</p>

<p align="center">
Figure 6: Texas expected behavior regarding CO2 emission and the predicted emission levels according to Texas average gas prices.  
</p>

### Discussion

The electric vehicle market is expected to grow to an unprecedented market value of $194.20 billion by 2027. With such a projected market growth, having a clear understanding of the factors affecting sales and the overall environmental impact of the market growth is of indispensable importance to investors, market analysts, and consumers.   

As seen by the relative risk categorization of states based on the k-means clustering, most states are classified as low or medium risk. The distinguishment between these 2 risk categories may be contributed by the large amounts of suburban communities in states such as Georgia, North Carolina, and Virginia, where vehicle usage is high as well as a larger population concentration. The introduction of three additional features from the midterm report to the final version of the project added a much need robustness to the algorithm and changed the classification distribution of the states, with a more even distribution between low and mid risk states, as well as identifying Florida as a high-risk state.  California, Texas, and Florida are designated as the three high risk states due to the states’ incredibly high CO2 emissions as well as an increase in emissions in the case of Texas. In fact, the three states account for nearly 30% of the transportation CO2 emissions in 2018, with Texas accounting for 39.85% of the increase in CO2 levels since 2011. To combat this, EV sales promotion should be directed strenuously towards Texas and an increase in gasoline prices should be encouraged across all three states to help curtail both the current high transportation CO2 emissions as well as future increases. 

It is interesting to note that the Random Forest algorithm identified single commuters as the most important feature to address regarding CO2 mitigation. This directly implies that there is a disproportionate number of vehicles owned per person and that investing in public transportation would have a greater impact in the race to diminish CO2 emissions than additional sales of PHEV, HEV, or EV. The public transportation system in the City of Atlanta can be used as proof of the inefficiency of American public transportation as denoted by the preference of students to use UBERs, LYFTs, instead of MARTA's buses and subway system to move around the city.  There is also a greater popularity found in registered PHEV, being the second largest emission mitigation feature. There are several potential reasons for this, ranging from a customer's preference to hear their engine while driving and a preference towards large engines, to the reality that the first electric vehicle did not have a great battery range and the fear of running out of battery while driving. In this aspect, we expect advances in battery technology to increase the importance of EV over other features. 

The current multivariate linear regression model, as evidenced by the positive EV sales coefficient seen in Equation 1, proves that the current EV sale is not large enough create a meaningful impact on the CO2 emissions from the transportation industry. This can be contributed to the exponential increase in internal combustion engine (ICE) sales and their subsequent increase in carbon emission. This is similarly seen in Figure 6, where it can be seen how lower gas prices contribute to a great amount of ICE vehicles on the road and a greater CO2 emission level 

Another notable factor that diminishes the validity of our linear model is the exclusion of hybrid electric vehicles and hydrogen fueled vehicles from the electric vehicle data that is counted towards the total ICE car sale data. While still contributing to CO2 emission, HEV are the second most important emission mitigation feature. A total grouping of vehicles with alternative energy requirements, grouped under the term advanced technological vehicle (ATV) would provide a clearer trend and would facilitate the prediction of future market growth.  

The polynomial regression models showed the importance of gas prices when considering the number of vehicles in circulation and the CO2 emission levels. It is interesting to note that the decrease in emission level between 2002-2012 correspond to an increase in gas prices, while the decrease in gas prices from 2012 onwards had such an impact on CO2 emissions levels that even the introduction of EV, HEV, and PHEVs did nothing to mitigate the increase of emission levels. 

### Conclusion

The premise behind the project was based on whether an increase in advanced technology vehicle sales could positively impact the rising CO2 emissions within the transportation industry. Based on the calculated values from the linear regression on the sales and emission data, it is determined that the volume of EV sales is not significant to overcome the impact of the marked increase in total vehicle sales bolstered by the prolonged advantage of the lowest gas prices in the last 15 years.   

The k-means algorithm creates a risk categorization that groups each state based on its transportation CO2 emissions. This identifies which states would benefit from a marked increase in EV sales. Based on their high-risk categorization, it is recommended that EV sale promotions be emphasized in California, Florida, and Texas. Texas specifically has shown the greatest increase in transportation CO2 emissions since 2010 in addition to having the greatest current CO2 emissions based on emissions last recorded in 2018.  

With the introduction of gasoline prices, a more detailed analysis and prediction model can be carried out by modeling scenarios where the decrease in gas prices continue with the same behavior, scenarios where the gas price stagnates, and scenarios where the gas price increases. The inclusion of gas prices allowed for a clearer understanding of the past and current automotive market. Taking that into account, the regression models were carried out on the two highest risk states, and on a nationwide scale. From these models, future decreases in CO2 emission were predicted for California and the United States overall, yet it also predicted future increases in CO2 in the state of Texas. This proves the fact that gasoline and the petroleum industry have a stronger impact on the automotive market than advances in ATV technology. 

### References

[1] “Sources of Greenhouse Gas Emissions,” EPA, 09-Sep-2020. [Online]. Available: https://www.epa.gov/ghgemissions/sources-greenhouse-gas-emissions#transportation.  [Accessed: 01-Oct-2020].  

[2] N. Popovich and D. Lu, “The Most Detailed Map of Auto Emissions in America,” The New York Times, 10-Oct-2019. [Online]. Available: https://www.nytimes.com/interactive/2019/10/10/climate/driving-emissions-map.html.  [Accessed: 01-Oct-2020].  

[3] Office of Transportation and Air Quality, A. Hula, R. French, A. Maguire, A. Bunker, and T. Rojeck, Environmental Protection Agency, 2020. Available: https://nepis.epa.gov/Exe/ZyPDF.cgi?Dockey=P100YVFS.pdf   

[4] Sullivan, C. (2019, February 05). National Climate Assessment: States and cities are already reducing carbon emissions to save lives and dollars: NOAA Climate.gov. Retrieved December 08, 2020, from https://www.climate.gov/news-features/featured-images/national-climate-assessment-states-and-cities-are-already-reducing  

### Datasets

[1] Transportation energy-related carbon dioxide emissions, https://www.eia.gov/environment/emissions/state/excel/transportation.xlsx   

[2] U.S. Light-Duty Advanced Technology Vehicle (ATV) Sales* (2011–2019), https://autoalliance.org/energy-environment/advanced-technology-vehicle-sales-dashboard/  

[3] Overall U.S. Auto Industry Sales Figures, https://www.goodcarbadcar.net/usa-auto-industry-total-sales-figures/  

[4] Alternative Fuel Stations, https://www.bts.gov/alternative-fuel-stations  

[5] Commute Mode, https://www.bts.gov/commute-mode  

[6] Alternative Fuel Stations, https://www.bts.gov/alternative-fuel-stations  

[7] State Highway Travel, https://www.bts.gov/state-highway-travel  

[8] U.S. All Grades All Formulations Retail Gasoline Prices (Dollars per Gallon), https://www.eia.gov/dnav/pet/hist/LeafHandler.ashx?n=PET&s=EMM_EPM0_PTE_NUS_DPG&f=A  

[9] Weekly California All Grades All Formulations Retail Gasoline Prices  (Dollars per Gallon), https://www.eia.gov/dnav/pet/hist/LeafHandler.ashx?n=PET&s=EMM_EPM0_PTE_SCA_DPG&f=W  

[10] Weekly Texas Regular All Formulations Retail Gasoline Prices  (Dollars per Gallon), https://www.eia.gov/dnav/pet/hist/LeafHandler.ashx?n=PET&s=EMM_EPMR_PTE_STX_DPG&f=W  
