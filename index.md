
### Introduction/Background 

Transportation emissions are the biggest factor that keep developed countries from matching the sustainability and pollution goals described in the Paris Agreement. It is currently responsible for 28% of all carbon dioxide emissions in the United States and has seen an incredible expansion in the last 30 years, especially in metropolitan cities, like Atlanta, that have seen an 84% overall increase in CO2 emissions. To curtail the rising trend, the Environmental Protection Agency annually imposes a lower CO2 emission limit, forcing companies to invest millions of dollars to make vehicle engines more fuel efficient. This said, some car manufacturers, like Volkswagen, have seen emission increases due to a “large shift towards sport utility vehicles commonly referred to as SUVs” and an overall sale increase throughout the years [3]. This has also been attributed to low gas prices, and this increase in low gas mileage vehicle sales is attributed to the subsequent increase in CO2 transportation emissions [2]. To decrease pollution levels and match the EPA’s emission limit, several companies are investing in electric (EV) and hybrid electric vehicles (HEV). With a rising electric vehicle popularity, there is an expected negative correlation between electric vehicle sales and CO2 transportation emissions.    

### Problem Definition

To help determine the role EV sales has in curtailing CO2 emissions, this project will attempt to develop a correlation between yearly electric vehicle sales and CO2 transportation emissions to predict CO2 emissions based on future EV sales. Due to increasing sales of other gas-powered vehicles, the direct relationship between current EV sales on transportation CO2 emissions is still unknown. Analogously, there is no model predicting future CO2 emissions based off the increasing trend of EV sales relative to non-EV sales. This project will aim to create one by creating regression models mapping CO2 emissions to corresponding EV sales and non-EV sales of the same year. Similarly, there will be an attempt to predict the increase in the volume of future sales based on past sale trends and identify whether there is an increase of EV sales when compared against the sales of internal combustion engine vehicles. Lastly, a clustering analysis will be performed to determine high, medium, and low risk states according to their CO2 emissions history. This will identify states to focus promoting efforts towards to increase EV sales. 

### Data Collection

To develop models relating EV sales to transportation CO2 emissions, datasets were collected that detailed the yearly recorded measurements of transportation CO2 levels as well as vehicle sales - EV and non-EV sales - for each state within the United States. The CO2 emissions dataset was referenced from data.gov to ensure the collection of accurate government-sponsored data about the CO2 emissions in the United States. CO2 emissions were measured by million metric tons (Mt). External websites such as Auto Alliance were used to collect EV and non-EV sales data for each state, where sales are measured by number of vehicles. 

The datasets detailing vehicles sales and transportation CO2 emissions were cleaned for corresponding clustering and regression models. Specifically, data corresponding to the time period of 2011 to 2018 was extracted due to that being the recorded starting period of EV sales due to the short history of modern electrical vehicles. For subsequent clustering, the CO2 emissions data was further cleaned to include 2 features with each state being a datapoint: 1) transportation CO2 emissions during 2018 2) net change in transportation CO2 emissions from 2011-2018. These features were chosen because they detail the current state and trends of emissions for each state. Therefore, states can be clustered into risk categories by current emissions and future paths. For regression models, the data for each state was summed to generate total, nationwide EV sales, non-EV sales, and CO2 emissions as seen in Table 1. These 3 features were chosen to create a multivariate linear regression model relating CO2 emissions to both EV sales and non-EV sales. This is due to the amount sales of non-EV vehicles also impacting CO2 emissions as aforementioned. In addition, the temporal dataset of total, nationwide transportation CO2 emissions and EV sales will be used to create additional regression models for prediction of future CO2 emissions and EV sales. 

<p align="center">
  Table 1: Linear Regression Model Data
</p>
<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/images/Picture1.png?raw=true">
</p>

### Methods

To develop a relationship between yearly electric vehicle sales and CO2 transportation emissions, several regression models were developed. This offered a novel model that can be used to predict future transportation CO2 emissions based off the trends of EV sales relative to non-EV sales. Specifically, both a linear and polynomial regression model were developed. Creating a linear fit will effectively provide a preliminary model providing a general correlation between transportation CO2 emissions and EV sales and Non-EV sales. Generating a subsequent polynomial model will be more effective in creating a model for predicting CO2 emissions based on vehicle sales due to the expected relationship between CO2 emissions and EV and non-EV sales being non-linear. This is due to CO2 emissions created by road vehicles varying as a result of different gas mileages. Similarly, there will be an attempt to predict the increase in the volume of future sales based on past sale trends and identify whether there is an increase of EV sales when compared against the sales of internal combustion engine vehicles. A regression analysis will also be developed for the temporal data of transportation CO2 emissions and EV sales to predict corresponding CO2 emissions and EV sales of future years. A polynomial regression is effective due to the temporal data not being linear. 

To cluster each state into low-, medium-, and high-risk categories based on their transportation CO2 emissions, a k-means clustering algorithm was used. This is due to the risk designation being a hard categorization, so k-means is deemed effective over other clustering techniques such as gaussian mixture model. As previously mentioned, the features for this clustering are 1) transportation CO2 emissions during 2018 2) net change in transportation CO2 emissions from 2011-2018. This allows the clustering/risk categorization to be done based on both the current state and trends of emissions for each state. This new approach will help define states where EV sales should be promoted most seriously. 

### Results

A multivariate linear regression model, observed in Figure 1, relates the nationwide transportation CO2 emissions to the EV and non-EV sales. As seen by Equation [1], the multivariate linear model details the transportation CO2 emissions having a positive relationship with both EV and Non-EV sales, even though EV do not contribute to CO2 emissions in real life. Specifically, this linear model predicts the one EV car sale to contribute 3.87e-05 Mt of CO2 (38700 Kg) a year. 

<p align="center">
  CO2 emissions =  3.87e−05 (EV Sales) +  2.17e−05 (Non−EV Sales) +  1499.46 [1] 
</p>

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/images/picture3.png?raw=true">
</p>
<p align="center">
  Figure 1: Linear Regression between CO2 Emissions, EV sales, and Non-EV sales 
</p>

As seen in Figure 2, all 50 US states as well as the District of Columbia have been clustered into low-, medium-, and high-risk categories based on their transportation CO2 emissions relative to each other. High recent CO2 emissions as well as high increases in CO2 emissions indicate high risk. The individual designations of each state can be seen in Table 2. Majority of states (34) are categorized to be low risk while 15 states make up medium risk categories, which includes the state of Georgia. While most medium and low risk states are clustered closely, the high-risk states of California and Texas account generate relatively much larger transportation CO2 emissions with Texas additionally experiencing much larger increases from 2011-2018. The change in emissions in California is comparable to low-risk and medium-risk states, but experiences much higher absolute, yearly transportation CO2 emissions. 

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/images/Picture2.png?raw=true">
</p>

<p align="center">
Figure 2: K-means risk clustering of states based on transportation CO2 emissions 
</p>

<p align="center">
  Table 2: List of US states and risk designation 
</p>

<p align="center">
  <img src="https://github.com/ykim879/machine.learning.project/blob/gh-pages/images/picture4.png?raw=true">
</p>

### Discussion

The electric vehicle market is expected to grow to an unprecedented market value of $194.20 billion by 2027. With such a projected market growth, having a clear understanding of the factors affecting sales and the overall environmental impact of the market growth is of indispensable importance to investors, market analysts, and consumers.  

The current model, as evidenced by the positive EV sales coefficient seen in Equation 1, proves that the current EV sale is not large enough create a meaningful impact on the C02 emissions from the transportation industry. This can be contributed to the exponential increase in internal combustion engine (ICE) sales and their subsequent increase in carbon emission. Another notable factor is the exclusion of hybrid electric vehicles and hydrogen fueled vehicles from the electric vehicle data that is counted towards the total ICE car sale data. A total grouping of vehicles with alternative energy requirements, grouped under the term advanced technological vehicle (ATV) may also provide a clearer trend and may facilitate the prediction of future market growth. 

As seen by the relative risk categorization of states based on the k-means clustering, majority of states are classified as low or medium risk. The distinguishment between these 2 risk categories may be contributed by the large amounts of suburban communities in states such as Georgia, North Carolina, and Florida. where vehicle usage is high. California and Texas are designated as the two high risk states due to the states’ incredibly high CO2 emissions as well increase in emissions in the case of Texas. In fact, the two states account for 23.78% of the transportation CO2 emissions in 2018, with Texas accounting for 39.85% of the increase in CO2 levels since 2011. Therefore, EV sales promotion should be directed most seriously in Texas to help curtail both the current high transportation CO2 emissions as well as future increases. 

Another possible result of the failed model is due to insufficient data on more meaningful factors such as gasoline prices. Gasoline price is currently one of the biggest international factors that influence the worldwide economy. As such, leaving out the progression of gasoline prices might be a point of error within our model. It is believed that the inclusion of an additional parameter will add enough robustness to our algorithm to make a more accurate prediction of the future EV market behavior and its impact on CO2 emission levels. 


### Conclusion

The premise behind the project was based on whether an increase on electric vehicle sales could positively impact the rising CO2 emissions within the transportation industry. Based on the calculated values from the linear regression on the sales and emission data, it is determined that the volume of EV sales is not significant to overcome the impact of the marked increase in total vehicle sales bolstered by the prolonged advantage of the lowest gas prices in the last 15 years.  

The k-means algorithm creates a risk categorization that groups each state based on its transportation CO2 emissions. This identifies which states would benefit from a marked increase in EV sales. Based on their high-risk categorization, it is recommended that EV sale promotions be emphasized in California and Texas. Texas specifically has shown the greatest increase in transportation CO2 emissions since 2010 in addition to having the greatest current CO2 emissions based on emissions last recorded in 2018. 

Future analysis for the project must be conducted to model the relationship more accurately between transportation CO2 emissions and EV sales. This will be done by extending the current multivariate linear regression into a polynomial regression. In addition, sales of low-gas mileage vehicles have also been attributed to low gas prices [2], which may act as a new feature in the regression model. With the introduction of gasoline prices, a more detailed analysis and prediction model can be carried out by modeling scenarios where the decrease in gas prices continue with the same behavior, scenarios where the gas price stagnates, and scenarios where the gas price increases. The inclusion of gas prices will allow for a clearer understanding of the current and past market behavior while adding an additional form of complexity and robustness to our data for a more accurate prediction. A polynomial regression will also be extended to the temporal data of transportation CO2 emissions as well as EV sales to predict future sales. 

### References

[1] “Sources of Greenhouse Gas Emissions,” EPA, 09-Sep-2020. [Online]. Available: https://www.epa.gov/ghgemissions/sources-greenhouse-gas-emissions#transportation.  [Accessed: 01-Oct-2020]. 

[2] N. Popovich and D. Lu, “The Most Detailed Map of Auto Emissions in America,” The New York Times, 10-Oct-2019. [Online]. Available: https://www.nytimes.com/interactive/2019/10/10/climate/driving-emissions-map.html.  [Accessed: 01-Oct-2020]. 

[3] Office of Transportation and Air Quality, A. Hula, R. French, A. Maguire, A. Bunker, and T. Rojeck, Environmental Protection Agency, 2020. Available: https://nepis.epa.gov/Exe/ZyPDF.cgi?Dockey=P100YVFS.pdf  

### Datasets

[1] Transportation energy-related carbon dioxide emissions, https://www.eia.gov/environment/emissions/state/excel/transportation.xlsx  

[2] U.S. Light-Duty Advanced Technology Vehicle (ATV) Sales* (2011–2019), https://autoalliance.org/energy-environment/advanced-technology-vehicle-sales-dashboard/ 

[3] Overall U.S. Auto Industry Sales Figures, https://www.goodcarbadcar.net/usa-auto-industry-total-sales-figures/ 
