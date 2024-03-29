# Justin Giovatto Portfolio

 - ## Experienced Marketing and Project Management Professional, Recent Flatiron School Data Science Graduate.
![Screen Shot 2021-11-11 at 2 33 45 PM](https://user-images.githubusercontent.com/66973223/141365994-0ebf86fe-e02b-47a9-bcf7-e2c61eeb2dd9.png)
## justin.giovatto@gmail.com

# Project 1 - Stock Market Data Analysis
## Business Objective
A stock market investor is looking to invest in a portfolio consisting of three technology companies, three healthcare companies, as well as one cryptocurrency for the next six month period. The investor also would like to minimize risk in the protfolio.

## Data
The stock data used for this project is from the Yahoo Finance API. The top 10 stocks with at least 5 years of trading data, according to volume traded in the technology and healthcare sectors will be analyzed. Also the top 5 cryptocurrency stocks with at least 5 years of trading data, according to volume traded will also be analyzed. The start date for the stocks is January 1st, 2016 and the end date is June 1st, 2021. The stocks will then be broken up into individual dataframes as well as combined into three seperate dataframes according to sector. The stocks are formated into daily data and provides the following features: "High", "Low", "Open", "Close", "Volume", and "Adj Close". An additional column for "Stock" (name), "Returns", and "Cumulative Returns" will also be added onto the data for analysis.

![Screen Shot 2021-09-14 at 2 15 01 PM](https://user-images.githubusercontent.com/66973223/133312926-7576720c-99a5-4fd4-b1bb-c2ea1f5eadd3.png)
 - Apple appears to following a general upward trend which appears to be increasing since late 2019. Apple also appears to have a seasonal component with spikes during the early and late parts of the year.

![Screen Shot 2021-11-11 at 2 46 25 PM](https://user-images.githubusercontent.com/66973223/141359646-22c2aebc-a7ca-4bd6-971f-b6c40248d7aa.png)
 - United Health appears to be autocorrelated up to about 6 lags.

![Screen Shot 2021-11-11 at 2 51 01 PM](https://user-images.githubusercontent.com/66973223/141360030-3e74a401-0b53-406f-8ca6-5f65525c2c35.png)
 - Of the top three crypto stocks Dodgecoin looks to be the most volatile with high returns over 2.5 as well as many returns in the .5 to 1 range. Bitcoin and Ethereum look to have similar volatility though Bitcoin appears to be slightly more stable. Compared to the tech and tealthcare sectors, the cryptocurrencies are clearly the most volatile of the three with a much greater range of returns. 

![Screen Shot 2021-11-11 at 2 46 41 PM](https://user-images.githubusercontent.com/66973223/141359693-1d656e54-ac42-4593-bce9-11d11beff1f2.png)
 - Microsoft appears to follow a fairly steady upward 6 month trend, while Apple follows a similar trend despite a slight dip during 2019 and 2020, before finally beginning to pulling ahead of Microsoft in 2021. Overall Google follows a flatter upward trend than the other two before beginning to slightly increase in 2021. All three stocks appear to be following an upward 6 month trend. 

![Screen Shot 2021-11-11 at 2 46 50 PM](https://user-images.githubusercontent.com/66973223/141359716-a41cefcc-8d70-4b5e-bfb3-58f3f9821e79.png)
 - Overall United Health looks to have most steady increase in 6 month returns despite a slight dip in 2019. HCA seems to be the most volatile of the three, though it does appear to be sharply rising since late 2020. CVS looks to be experiencing a slow, flat downward trend over the past 5 years.

![Screen Shot 2021-11-11 at 2 46 58 PM](https://user-images.githubusercontent.com/66973223/141359746-0773cdae-bbfd-4a8c-8162-a4b66e1c9de5.png)
 - Overall Ethereum seems to be the most volatile of the three crypto stocks wit a sharp increase in 6 month trend during mid 2017 to mid 2018 before sharply dropping again until mid 2019 where it remained flat until late 2020 where it has since dramatically risen to an almost 2000% cumulative return. Bitcoin and Dogecoin also remained fairly flat until mid 2021 where Dogecoin sharply rose to about 900% cumulative return, while Bitcoin also began to steadily increase. Overall this could indicate that Crypto stocks are experiencing a sharp rise in cumulative returns and will be interesting to see if it continues going forward.

## Overview/Methods
This notebook will analyze the top ten tech and healthcare stocks according to volume traded as well the top five cryptocurrency stocks by volume traded. The stocks will then be analyzed according to past future returns dating back to January 2016. The stocks' volitility over that period will also be taken into account in order to analyze potential risk. A sarima model and Facebook Prophet model will then be run on each of the stocks in order to predict future returns over the next six month period. Model results will then be compared and analyzed, and portfolio investment reccomendations will then be provided based on the analysis.

![Screen Shot 2021-11-11 at 2 47 37 PM](https://user-images.githubusercontent.com/66973223/141359797-1d246782-7d7e-4ddf-8072-9259442f0473.png)
 - According to the SARIMA model forecast, the top tech stock was Nvidia with a predicted 25.83% increase over the next 6 month period.

![Screen Shot 2021-11-11 at 2 58 49 PM](https://user-images.githubusercontent.com/66973223/141361055-68bb68cb-9413-499b-917f-eeb6293f369f.png)

![Screen Shot 2021-11-11 at 2 47 46 PM](https://user-images.githubusercontent.com/66973223/141359817-f2c38cac-5e29-4d48-b77e-dc4874fe6e44.png)
 - The top healthcare stock according to the SARIMA model was Bio-Rad with a predicted increase of 5.17% over the next 6 month period.

![Screen Shot 2021-11-11 at 2 58 58 PM](https://user-images.githubusercontent.com/66973223/141361114-de5f955c-24f0-4393-8db5-3769c8f117c1.png)

![Screen Shot 2021-11-11 at 2 47 54 PM](https://user-images.githubusercontent.com/66973223/141359839-6be734ad-800f-429e-a975-3a5f298cce88.png)
 - The top cryptocurrency according to the SARIMA model was Dogecoin with a predicted increase of 4,534.25% over the next 6 month period.

![Screen Shot 2021-11-11 at 2 59 06 PM](https://user-images.githubusercontent.com/66973223/141361139-291721ef-521d-4dd1-a6f6-145b5963f5ec.png)

## Results & Conclusions

Based on the above model comparison charts, our two main Tech sector recommendations will be Nvidia and Tesla due to high SARIMA forecasts as well as high min. lower confidence interval predictions. Both these stocks feature the highest main evaluation metric forecasts. The third tech stock recommendation will be TSMC. This stock produces the third highest SARIMA 6 month forecast in comparison to the other stocks in the sector.  

For the healthcare sector I would recommend BIO, HCA, and UNH as these stocks are the highest healthcare stocks in terms of SARIMA forecast and min. lower confidence intervals as seen in the graph below.

Finally for the crypto sector recommendation, although DOGE has the highest SARIMA foercast it also has a significantly lower min. lower confidence interval than ETH, as observed in the above graph. Because avoiding risk is a big factor in choosing this portfolio I would instead recommend ETH over DOGE for this reason.

![Screen Shot 2021-09-14 at 2 19 10 PM](https://user-images.githubusercontent.com/66973223/133313840-9e68237a-8603-49b4-a215-f239e058ef52.png)

![Screen Shot 2021-09-14 at 2 19 24 PM](https://user-images.githubusercontent.com/66973223/133313892-e0e45f48-57cf-4e0a-8746-68af3de823b6.png)

![Screen Shot 2021-09-14 at 2 19 34 PM](https://user-images.githubusercontent.com/66973223/133313949-f1894a33-2bbe-4933-afeb-7c41b172ab8c.png)

* Top 3 Tech Stocks to invest in:
 1. Nvida
 2. Tesla
 3. TSMC
     
* Top 3 Healthcare Stocks to invest in:
 1. Bio-Rad
 2. United Health
 3. HCA
  
* Top Cryptocurrency to invest in:
 1. Ethereum
 
## Future Work
 - Would like to add another model type such as an RNN for further model comparisons.
 
 
 - Would like to analyze more stocks in each sector in order to find potentially better portfolio recommendations.
 
 
 - Would like to look into more stock evaluation metrics in order to improve recommendations further.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/Stock-Market-Analysis/blob/main/Stock-Market-Analysis.ipynb) 





# Project 2 - SyriaTel Customer Churn Analysis

## Overview
This project analyzes SyriaTel customer account data in order to build classifications models aimed at predicting customer churn. 
## Business Objective
SyriaTel, a telecommunications company, is interested in knowing the important factors in determining whether or not a customer will stay with the company. The primary goal of this notebook is to help SyriaTel keep current customers and offer business strategies on how to do so based on the analysis provided.  

## Data
The dataset contains relevant customer account data including:

  - The state of the customer.
    
  - The account length of the customer.
    
  - The customer's area code.
    
  - Whether or not the customer has an international plan.
    
  - Whether or not the customer has a voicemail plan.
    
  - The total day, evening, night, and international minutes of the customer.
    
  - The total day, evening, night, and international calls of the customer.
    
  - The total day, evening, night, and international charge of the customer.
    
  - The total customer service calls of the customer.
    
  - Whether or not the customer was 'true' or 'false' churn (true churn meaning that they have left the company, this will be the primary focus of the models).
  
  - The data contains no missing values.

![Screen Shot 2021-10-12 at 5 29 28 PM](https://user-images.githubusercontent.com/66973223/137032113-ee4ab177-ea09-490a-88b2-75942a2c066e.png)
 - Data contains significatly more 'false's than 'true's, this will need to be addressed later when building models in order to prevent class imbalance.

![Screen Shot 2021-10-12 at 5 30 06 PM](https://user-images.githubusercontent.com/66973223/137032197-4c16e344-a6ff-4009-b2af-c34d4b5820cc.png)
 - Internaional plan will need to be converted to a categorical feature.

![Screen Shot 2021-10-12 at 5 30 19 PM](https://user-images.githubusercontent.com/66973223/137032241-f790f235-7eec-41bb-9699-4ff578dd0a82.png)
 - Customer service calls does not appear to be evenly distributed. This feature could be relevant at predicting churn as cutomers who are unhappy with their service would likely make more customer service calls.

## Methods
* SyriaTel customer data will be used to create six different classification models to predict customer churn.

* The models will then be analyzed according to the precision metric.

* The best performing model will be analyzed for top feature importance.

* Business recommendations will then be presented. 

## Results & Conclusions
![Screen Shot 2021-10-12 at 7 35 40 PM](https://user-images.githubusercontent.com/66973223/137042873-202a3c36-4697-4bef-87eb-a32cafa073ef.png)

![Screen Shot 2021-10-12 at 7 15 41 PM](https://user-images.githubusercontent.com/66973223/137041678-44f948ea-d3fd-4d32-8c70-48added90f99.png)

![Screen Shot 2021-10-12 at 8 39 21 PM](https://user-images.githubusercontent.com/66973223/137047570-b9dafe95-b6d1-4dff-ade4-6377045a9d36.png)

![Screen Shot 2021-10-12 at 7 16 23 PM](https://user-images.githubusercontent.com/66973223/137041739-2c0f1955-42d0-4fc7-8028-11e0fd01781e.png)

![Screen Shot 2021-10-12 at 7 16 36 PM](https://user-images.githubusercontent.com/66973223/137041780-43fbd7f5-2831-4885-974e-93167d27bcff.png)

## Top Performing Model
The top performing model accorinding to the precision and ROC metrics was a Random Forest model using GridsearchCV in order to tune parameters. The top three features according to this model include:

1. Total Charge
2. Customer Service Calls
3. Total International Minutes

![Screen Shot 2021-10-12 at 7 16 49 PM](https://user-images.githubusercontent.com/66973223/137041812-425271eb-9281-4e06-9d19-2e62df834887.png)

![Screen Shot 2021-10-12 at 7 55 04 PM](https://user-images.githubusercontent.com/66973223/137044314-8f6c30e6-23eb-4544-ac28-577bc3b9cd6e.png)

## Model Comparison
![Screen Shot 2021-10-12 at 5 39 50 PM](https://user-images.githubusercontent.com/66973223/137032824-36860349-c232-4fac-acc2-35cd3932e7f4.png)

Based on the analysis, my main business recommendations are as follows:

1. Offer discounts/promotions to customers with higher than average total charge costs.

2. Offer discounts/promotions to customer who frequently call customer service. As well as improving customer service as a whole to better resolve issues. 

3. Create a competitive international plan to prevent international customers from leaving as well as attract more international customers overall.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/churn-analysis-project/blob/main/SyriaTel-Customer-Churn-Analysis.ipynb)




# Project 3 - New Jersey County Time Series Analysis

## Business Objective
A real estate investment firm is interested in knowing the top three New Jersey counties to invest in based on return on investment (ROI).
## Overview
This project analyzes a New Jersey Zillow dataset in order predict the top three counties to invest in over the next five year period according to forecasted ROI. This notebook will analyze past ROI data in order to compare with future forecasted ROI predictions. The model used for predicting future ROI will be a SARIMA model, which takes into account the seasonal nature of the real estate market. The data will then be broken out by county and will use a stepwise fit to find optimal model orders in order to minimize AIC and produce the most accurate model based on the data. The SARIMA models will then be fitted and will forecast 5 years into the future. The models will then be analyzed taking into account RMSE as an evaluation metric. The top three counties will then be reccomended based on these methods, as well as the main counties to avoid, and the county with the lowest initial investment. 

## Data
The data used in this notebook will be Zillow home data ranging from April 1st, 1996 through April 1st, 2018. The data contains home value information from the United States consisting of 14,723 columns and 272 rows. For the purposes of this project the data will be filtered to only include New Jersey data. The New Jersey data will then be seperated out by individual county in order to model each county for forecasted ROI. The data will also be grouped by month for a mean value of homes for each month. The data will first need to be converted into datetime objects in order to prepare it for time series modeling. The data will also need to be converted from wide to long format in order to make it easier to work with and interperet.

![Screen Shot 2021-11-12 at 10 41 32 AM](https://user-images.githubusercontent.com/66973223/141494041-2209e7d3-eda6-4cde-8e84-e4e8135a7e77.png)
 - Overall New Jersey home values appear to have sharply increased from 1996 through around 2006 before significantly dropping in value from 2008 to around 2012. This is likely due to the housing crisis and recession starting in 2008. Since around 2012 home values appear to be steadily increasing across the state as the economy began to steadily improve during this time period. Overall the data does not appear to be stationary as it follows a general upward trend.

![Screen Shot 2021-11-12 at 10 41 52 AM](https://user-images.githubusercontent.com/66973223/141494141-db2e6fa4-19e3-4011-82ec-431bc87d9cdb.png)
 - Looking at the decomposition chart, the data appears to follows a general upward  trend as expected. The data is also very seasonal, likely due to the seasonal nature of the real esate market in general.

![Screen Shot 2021-11-12 at 10 42 01 AM](https://user-images.githubusercontent.com/66973223/141494176-ec30639b-a36e-47f6-a808-ebe41c6cf2a8.png)
 - Autocorrelation graph shows the data is correlated up to about 20 lags.

![Screen Shot 2022-03-11 at 3 07 00 PM](https://user-images.githubusercontent.com/66973223/157951723-4a3ecb94-dcda-4646-8f33-b318068c27bb.png)
 - Overall the top three ROI counties appear to be following a general upward trend aside from the downturn due to the 2008 economic recession. Hudson county appears to have been hit the hardest by the recession but has since sharly bounced back. Also Cape May County had the overall highest average value close to 700,000 before the recession and did not get hit as hard as Hudson County. Monmouth County started at the highest average value in 1996 but has since been somewhere in the middle of the other two counties. Going forward it will be interesting to see if Cape May will get back to its highest point of 700,000 and whether Hudson County values will continue to sharly rise or will begin to level off.  

## Methods
* Data will be broken out by all 21 New Jersey counties in order to run SARIMA models on each.  

* The SARIMA models will then be run for each county after determing optimal model order by running a stepwise fit.  

* Models will then be analyzed by county according to forecasted ROI.

* Business recommendations will then be presented.

![Screen Shot 2021-11-12 at 10 42 28 AM](https://user-images.githubusercontent.com/66973223/141494325-dac78df2-11c4-4bfe-9278-d44f3c42887f.png)

![Screen Shot 2021-11-12 at 10 42 49 AM](https://user-images.githubusercontent.com/66973223/141494358-018cabab-8cc8-4d84-85e2-2947d944346b.png)

![Screen Shot 2021-11-12 at 10 42 59 AM](https://user-images.githubusercontent.com/66973223/141494388-db07ae73-f633-434e-8b74-a7178ee26165.png)

## Results & Conclusions  

Based on the analysis, my main business recommendations are as follows:

1. Invest in Salem, Sussex, and Passaic County for the highest forecasted ROI returns. 
2. Strongly reccommend to invest in Salem County due to its lowest initial cost of just over 150,000 dollars along with the overall highest forecasted ROI of 121%, almost double the next highest forecast.
3. Recommend avoiding past top ROI counties including Hudson, Cape May, and Monmouth County. Despite the large past ROI data from these counties they may have leveled off in terms of value and likely will not be good investment options going forward.

![Screen Shot 2021-11-12 at 10 48 31 AM](https://user-images.githubusercontent.com/66973223/141494726-0b5609ee-dc91-4dbd-a794-ad88f7527823.png)

![Screen Shot 2021-11-12 at 10 49 02 AM](https://user-images.githubusercontent.com/66973223/141494825-b49405f5-b47e-478f-a89b-06731b3e2c1a.png)

![Screen Shot 2021-11-12 at 10 49 35 AM](https://user-images.githubusercontent.com/66973223/141494933-5d02d0ef-17cf-4851-a07e-dc05dfa57a7e.png)

## Future Work
1. Add another model type such as a RNN in order to compare its forecasts with the SARIMA models used here and check for similarities/differences between the models.
2. Go deeper into the analysis by modeling the top counties by their cities in order to determine the top ROI cities within the counties thereby providing even more targeted recommendations with regard to where to invest.
3. Take into account another evaluation metric along with ROI such as risk in order to provide more detailed investment recommendations.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/zillow-time-series-analysis/blob/main/zillow-time-series-analysis.ipynb)




# Project 4 - King County Home Value Analysis

## Overview
This notebook will analyze data from the King County House Sales dataset. This dataset contains various information on homes in King County, Washington. I will use this data in order to create linear regression models with the purpose of determining which features are most relevant in predicting home values. I will then examine the models' output and compare and contrast to determine which model performs best according to the R-Squared and Mean Absolute Error metrics. 
## Business Objective
Hypothetical Situation: A King County real estate agency is looking to provide advice to home owners on what factors are most important in determining the value of their home. Using several multiple linear regression models I will examine which independant variables are most useful at predicting the dependant variable of home price. The regression models will help in providing home owners with relevant information regarding the price of their home should they be interested in listing their home with the real estate agency.  

## Data
Data from the King County house sales dataset contains the following information regarding homes in King County: 

* id - unique identifier for a home

* dateDate - date home was sold

* pricePrice - home sale price

* bedroomsNumber - number of bedrooms

* bathroomsNumber - number of bathrooms

* sqft_livingsquare - footage of the home

* sqft_lotsquare - footage of the lot

* floorsTotal - total number of levels in home

* waterfront - home which has a view to a waterfront

* view - has been viewed by potential buyers

* condition - overall condition of the home

* grade - overall grade given to the housing unit, based on King County grading system

* sqft_above - square footage of house apart from basement

* sqft_basement - square footage of the basement

* yr_built - year home was built

* yr_renovated - year home was renovated

* zipcode - zip

* lat - Latitude coordinate

* long - Longitude coordinate

* sqft_living15 - square footage of interior housing living space for the nearest 15 neighbors

* sqft_lot15 - square footage of the land lots of the nearest 15 neighbors

![Screen Shot 2021-11-11 at 10 00 12 AM](https://user-images.githubusercontent.com/66973223/141325768-e5559cdd-e573-4381-9f1c-5f25c6dbbe8d.png)
 - The data is not evenly distributed for several columns. Will analyze this further and need to address later on for increased model accuracy. 

![Screen Shot 2021-11-11 at 10 18 28 AM](https://user-images.githubusercontent.com/66973223/141325822-7a2c8567-eeda-457c-84be-194286ede13e.png)
 - Several features such as sqft_lot and sqft_lot15 are closely related to each other and will need to be seperated when building models in order to prevent multicollinearity.

![Screen Shot 2021-11-11 at 10 00 24 AM](https://user-images.githubusercontent.com/66973223/141325861-50c19aca-5e95-4270-ae8d-46d6cae85c00.png)
 - Price contains outliers and is skewed to the right. Will address this by removing outliers.

## Methods
Using columns from the data provided I will build four unique linear models. I will then split the data into training and testing data. The models will be trained using the training data and then evaluated on the testing data to determine their accuracy. The accuracy of these models will be determined mainly by r-squared, mean absoluate error, mean squared error, and root mean squared error. After determining the accuracy of these model I will then evaluate the coefficients in order to determine which features are most important in determining true home value.

![Screen Shot 2021-11-11 at 10 00 47 AM](https://user-images.githubusercontent.com/66973223/141325939-00d9b756-20df-4752-9ed7-c95a400aa9a7.png)
 - According to Model A the top feature for determining price is square foot living, followed by grade and year built.

![Screen Shot 2021-11-11 at 10 39 56 AM](https://user-images.githubusercontent.com/66973223/141326061-a6f9691f-7c9d-4e3a-b747-117bf2e3ae35.png)
 - The actual vs. predicted chart shows that Model A does not appear to follow a strong linear pattern.

![Screen Shot 2021-11-11 at 10 01 21 AM](https://user-images.githubusercontent.com/66973223/141326213-e22d39fb-d38a-4ec7-9973-c7f83b3090e7.png)
 - According to Model B the top ten features for determining price are all zip codes.
 
![Screen Shot 2021-11-11 at 10 41 41 AM](https://user-images.githubusercontent.com/66973223/141326319-a8bbb5dd-fb0a-4d7a-b57c-ab02a8cacd71.png)
- Similar to Model A, Model B also does not appear to follow a strong linear pattern. The next model will remove outliers from the data to see if this improves model performance. 

![Screen Shot 2021-11-11 at 10 43 01 AM](https://user-images.githubusercontent.com/66973223/141326600-1d716403-525c-43fa-805f-e1264a59f118.png)
 - The most important feature according to Model C is square foot living followed by zip codes. 
 
![Screen Shot 2021-11-11 at 10 43 14 AM](https://user-images.githubusercontent.com/66973223/141326646-e41f727f-ae2a-4343-abe5-1937d7d32420.png)
 - Model C also follows a somewhat better linear pattern than both Model's A and B.
 
![Screen Shot 2021-11-11 at 10 43 27 AM](https://user-images.githubusercontent.com/66973223/141326678-ca05176d-db42-468d-8a13-a8de352a0cc5.png)
 - According to Model D the most important feature for predicting home price is Grade, followed by Distance from Seattle and Year Built.
 
![Screen Shot 2021-11-11 at 10 43 37 AM](https://user-images.githubusercontent.com/66973223/141326707-ff29c570-0257-4c06-ab7e-20135fcd604d.png)
 - Model D also follows a somewhat better linear pattern than the earlier models.

## Results & Conclusions  

The most reliable model was Model D which was able to predict home prices within $106,695 of the true home price. The R-squared for Model D was .655, with a Skew of 1.181, and Kurtosis of 6.691. Model D also produced a Mean Squared Error of 21,624,092,902 as well as a Root Mean Squared Error of 147,051.

While Models B and C produce the highest R-Squared metric, they also have a high skew and kurtosis likely due to the presence of outliers as well as the uneven distribution of homes within the zip code categorial columns. Once the outliers and zip code columns were removed for Model D, both the skew and kurtosis significantly decreased making for a more reliable model.

Aside from zip codes; Square Foot Living, Grade, and Year Built all appear in the top three features for multiple models making these features the most important in predicting home price according to the models. Also once zip codes were replaced with the new 'Distance from Seattle' feature in Model D, we can see that this feature ranked second in terms of importance.

According to the models we can infer that home size, location, age, and 'grade' are the most important features in accurately predicting home value for King County.

![Screen Shot 2021-11-11 at 10 45 52 AM](https://user-images.githubusercontent.com/66973223/141327441-cbb71254-eefb-48dd-8f2d-6ce1535fe720.png)
 - Models B and C both feature the highest R-Squared at .744 each. While Model A Features the lowest R-Squared at .623. Model D, the most accurate model in terms of skew and kurotsis comes in at .655.

![Screen Shot 2021-11-11 at 10 46 02 AM](https://user-images.githubusercontent.com/66973223/141327529-b6b306b2-4386-4739-91e1-6c355f036de5.png)
 - Overall the best MAE score was Model C, which on average predicts home values within 83,185 dollars of the actual home value. While the worst performing model according to MAE was model A, which on average predicts home values within 145,718 dollars of the actual home value. 

![Screen Shot 2022-01-07 at 11 23 52 AM](https://user-images.githubusercontent.com/66973223/148574279-3e236df9-b0ef-4c9e-bd77-49faccadc9cc.png)
 - According to the graph, as sqaure foot living increases the price of the home also tends to increase.
 
 - Square Foot Living was the top feature in both models A and C.

![Screen Shot 2022-01-07 at 11 24 08 AM](https://user-images.githubusercontent.com/66973223/148574391-43efce99-673b-442d-a51f-c82f4f998cd4.png)
 - According to the graph, as the 'grade' of the home increases the price of the home also tends to increase.
 
 - Grade was the top feature of Model D as well as the second most important feature for Model A.

![Screen Shot 2022-01-07 at 11 24 23 AM](https://user-images.githubusercontent.com/66973223/148574491-e006b64e-5502-4f83-b439-1d85de56d7ee.png)
 - According to the graph, as the distance from Seattle decreases the price of the home tends to generally increase.
 
 - Distance from Seattle was the second most important feature for Model D.

![Screen Shot 2022-01-07 at 11 24 45 AM](https://user-images.githubusercontent.com/66973223/148574532-74a8c28b-e056-4867-b2c5-caa9ab46b0ed.png)
- According to the graph, as the year the home was built increases the price of the home also tends to generally increase.

- Year Built was the third most important feature for both Models A and D.

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/home-sales-analysis/blob/main/home-sales-analysis.ipynb) 

For additional information contact Justin Giovatto at justin.giovatto@gmail.com


