# Justin Giovatto Portfolio

## Project 1 - Stock Market Data Analysis
## Business Objective
A stock market investor is looking to invest in a portfolio consisting of three technology companies, three healthcare companies, as well as one cryptocurrency for the next six month period. The investor also would like to minimize risk in the protfolio.

## Data
The stock data used for this project is from the Yahoo Finance API. The top 10 stocks with at least 5 years of trading data, according to volume traded in the technology and healthcare sectors will be analyzed. Also the top 5 cryptocurrency stocks with at least 5 years of trading data, according to volume traded will also be analyzed. The start date for the stocks is January 1st, 2016 and the end date is June 1st, 2021. The stocks will then be broken up into individual dataframes as well as combined into three seperate dataframes according to sector. The stocks are formated into daily data and provides the following features: "High", "Low", "Open", "Close", "Volume", and "Adj Close". An additional column for "Stock" (name), "Returns", and "Cumulative Returns" will also be added onto the data for analysis.

![Screen Shot 2021-09-14 at 2 15 01 PM](https://user-images.githubusercontent.com/66973223/133312926-7576720c-99a5-4fd4-b1bb-c2ea1f5eadd3.png)

![Screen Shot 2021-11-11 at 2 46 25 PM](https://user-images.githubusercontent.com/66973223/141359646-22c2aebc-a7ca-4bd6-971f-b6c40248d7aa.png)

![Screen Shot 2021-11-11 at 2 51 01 PM](https://user-images.githubusercontent.com/66973223/141360030-3e74a401-0b53-406f-8ca6-5f65525c2c35.png)

![Screen Shot 2021-11-11 at 2 46 41 PM](https://user-images.githubusercontent.com/66973223/141359693-1d656e54-ac42-4593-bce9-11d11beff1f2.png)

![Screen Shot 2021-11-11 at 2 46 50 PM](https://user-images.githubusercontent.com/66973223/141359716-a41cefcc-8d70-4b5e-bfb3-58f3f9821e79.png)

![Screen Shot 2021-11-11 at 2 46 58 PM](https://user-images.githubusercontent.com/66973223/141359746-0773cdae-bbfd-4a8c-8162-a4b66e1c9de5.png)

## Overview/Methods
This notebook will analyze the top ten tech and healthcare stocks according to volume traded as well the top five cryptocurrency stocks by volume traded. The stocks will then be analyzed according to past future returns dating back to January 2016. The stocks' volitility over that period will also be taken into account in order to analyze potential risk. A sarima model and Facebook Prophet model will then be run on each of the stocks in order to predict future returns over the next six month period. Model results will then be compared and analyzed, and portfolio investment reccomendations will then be provided based on the analysis.

![Screen Shot 2021-11-11 at 2 47 37 PM](https://user-images.githubusercontent.com/66973223/141359797-1d246782-7d7e-4ddf-8072-9259442f0473.png)

![Screen Shot 2021-11-11 at 2 47 46 PM](https://user-images.githubusercontent.com/66973223/141359817-f2c38cac-5e29-4d48-b77e-dc4874fe6e44.png)

![Screen Shot 2021-11-11 at 2 47 54 PM](https://user-images.githubusercontent.com/66973223/141359839-6be734ad-800f-429e-a975-3a5f298cce88.png)

![Screen Shot 2021-11-11 at 2 58 49 PM](https://user-images.githubusercontent.com/66973223/141361055-68bb68cb-9413-499b-917f-eeb6293f369f.png)

![Screen Shot 2021-11-11 at 2 58 58 PM](https://user-images.githubusercontent.com/66973223/141361114-de5f955c-24f0-4393-8db5-3769c8f117c1.png)

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
  - The state the customer is from
    
  - The account length of the customer
    
  - the customer's area code
    
  - Whether or not the customer has an international plan
    
  - Whether or not the customer has a voicemail plan
    
  - The total day, evening, night, and international minutes of the customer
    
  - The total day, evening, night, and international calls of the customer
    
  - The total day, evening, night, and international charge of the customer
    
  - The total customer service calls of the customer
    
  - Whether or not the customer was 'true' or 'false' churn (true churn meaning that they have left the company, this will be the primary focus of the models)
  
  - The data contains no missing values

![Screen Shot 2021-10-12 at 5 29 28 PM](https://user-images.githubusercontent.com/66973223/137032113-ee4ab177-ea09-490a-88b2-75942a2c066e.png)

![Screen Shot 2021-10-12 at 5 30 06 PM](https://user-images.githubusercontent.com/66973223/137032197-4c16e344-a6ff-4009-b2af-c34d4b5820cc.png)

![Screen Shot 2021-10-12 at 5 30 19 PM](https://user-images.githubusercontent.com/66973223/137032241-f790f235-7eec-41bb-9699-4ff578dd0a82.png)

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

![Screen Shot 2021-09-14 at 1 57 56 PM](https://user-images.githubusercontent.com/66973223/133309726-69f00566-9c1c-49d7-9541-a7b432726595.png)

## Methods
* Data will be broken out by all 21 New Jersey counties in order to run SARIMA models on each.  

* The SARIMA models will then be run for each county after determing optimal model order by running a stepwise fit.  

* Models will then be analyzed by county according to forecasted ROI.

* Business recommendations will then be presented. 

## Results & Conclusions  

Based on the analysis, my main business recommendations are as follows:

1. Invest in Salem, Sussex, and Passaic County for the highest forecasted ROI returns. 
2. Strongly reccommend to invest in Salem County due to its lowest initial cost of just over 150,000 dollars along with the overall highest forecasted ROI of 121%, almost double the next highest forecast.
3. Recommend avoiding past top ROI counties including Hudson, Cape May, and Monmouth County. Despite the large past ROI data from these counties they may have leveled off in terms of value and likely will not be good investment options going forward.

![Screen Shot 2021-09-14 at 1 58 18 PM](https://user-images.githubusercontent.com/66973223/133309829-449eb921-e64e-4158-98db-228ddf68faf2.png)

![Screen Shot 2021-09-14 at 1 58 40 PM](https://user-images.githubusercontent.com/66973223/133309857-a30a389a-7266-48b1-87a9-1ca06554f40d.png)

![Screen Shot 2021-09-14 at 1 58 51 PM](https://user-images.githubusercontent.com/66973223/133309877-50f6eb67-e70e-45fe-9920-f208ff0e0667.png)

![Screen Shot 2021-09-14 at 1 59 03 PM](https://user-images.githubusercontent.com/66973223/133309908-5116369e-7346-40b6-bedf-04a2eddf143b.png)
 
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

![Screen Shot 2021-11-11 at 10 18 28 AM](https://user-images.githubusercontent.com/66973223/141325822-7a2c8567-eeda-457c-84be-194286ede13e.png)

![Screen Shot 2021-11-11 at 10 00 24 AM](https://user-images.githubusercontent.com/66973223/141325861-50c19aca-5e95-4270-ae8d-46d6cae85c00.png)


## Methods
Using columns from the data provided I will build four unique linear models. I will then split the data into training and testing data. The models will be trained using the training data and then evaluated on the testing data to determine their accuracy. The accuracy of these models will be determined mainly by r-squared, mean absoluate error, mean squared error, and root mean squared error. After determining the accuracy of these model I will then evaluate the coefficients in order to determine which features are most important in determining true home value.

![Screen Shot 2021-11-11 at 10 00 47 AM](https://user-images.githubusercontent.com/66973223/141325939-00d9b756-20df-4752-9ed7-c95a400aa9a7.png)

![Screen Shot 2021-11-11 at 10 39 56 AM](https://user-images.githubusercontent.com/66973223/141326061-a6f9691f-7c9d-4e3a-b747-117bf2e3ae35.png)

![Screen Shot 2021-11-11 at 10 01 21 AM](https://user-images.githubusercontent.com/66973223/141326213-e22d39fb-d38a-4ec7-9973-c7f83b3090e7.png)

![Screen Shot 2021-11-11 at 10 41 41 AM](https://user-images.githubusercontent.com/66973223/141326319-a8bbb5dd-fb0a-4d7a-b57c-ab02a8cacd71.png)

![Screen Shot 2021-11-11 at 10 43 01 AM](https://user-images.githubusercontent.com/66973223/141326600-1d716403-525c-43fa-805f-e1264a59f118.png)

![Screen Shot 2021-11-11 at 10 43 14 AM](https://user-images.githubusercontent.com/66973223/141326646-e41f727f-ae2a-4343-abe5-1937d7d32420.png)

![Screen Shot 2021-11-11 at 10 43 27 AM](https://user-images.githubusercontent.com/66973223/141326678-ca05176d-db42-468d-8a13-a8de352a0cc5.png)

![Screen Shot 2021-11-11 at 10 43 37 AM](https://user-images.githubusercontent.com/66973223/141326707-ff29c570-0257-4c06-ab7e-20135fcd604d.png)

## Results & Conclusions  

The most reliable model was Model D which was able to predict home prices within $106,695 of the true home price. The R-squared for Model D was .655, with a Skew of 1.181, and Kurtosis of 6.691. Model D also produced a Mean Squared Error of 21,624,092,902 as well as a Root Mean Squared Error of 147,051.

While Models B and C produce the highest R-Squared metric, they also have a high skew and kurtosis likely due to the presence of outliers as well as the uneven distribution of homes within the zip code categorial columns. Once the outliers and zip code columns were removed for Model D, both the skew and kurtosis significantly decreased making for a more reliable model.

Aside from zip codes; Square Foot Living, Grade, and Year Built all appear in the top three features for multiple models making these features the most important in predicting home price according to the models. Also once zip codes were replaced with the new 'Distance from Seattle' feature in Model D, we can see that this feature ranked second in terms of importance.

According to the models we can infer that home size, location, age, and 'grade' are the most important features in accurately predicting home value for King County.

![Screen Shot 2021-11-11 at 10 45 52 AM](https://user-images.githubusercontent.com/66973223/141327441-cbb71254-eefb-48dd-8f2d-6ce1535fe720.png)

![Screen Shot 2021-11-11 at 10 46 02 AM](https://user-images.githubusercontent.com/66973223/141327529-b6b306b2-4386-4739-91e1-6c355f036de5.png)

![Screen Shot 2021-11-11 at 10 46 18 AM](https://user-images.githubusercontent.com/66973223/141327580-5fa81ce5-793c-4c7c-bbb1-f8387b6f4125.png)

![Screen Shot 2021-11-11 at 10 46 28 AM](https://user-images.githubusercontent.com/66973223/141327610-685ba56f-fee2-4c7d-83db-02bc07e99197.png)

![Screen Shot 2021-11-11 at 10 46 37 AM](https://user-images.githubusercontent.com/66973223/141327649-cb01690e-1de0-4a11-a6bb-ba229cad8076.png)

![Screen Shot 2021-11-11 at 10 46 46 AM](https://user-images.githubusercontent.com/66973223/141327678-95a29b4a-59a4-4582-b271-9fa5ac64e70d.png)

## For More Information
See the full analysis in the [Jupyter Notebook](https://github.com/jmg0144/home-sales-analysis/blob/main/home-sales-analysis.ipynb) 

For additional information contact Justin Giovatto at justin.giovatto@gmail.com


