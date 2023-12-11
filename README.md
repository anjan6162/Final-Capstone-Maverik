# Maverik Sales Forecasting

## 1. Business Problem Statement:

A retail convenience chain, Maverik, fuels adventures in more than 380 locations across 12 western states. Maverik is known for premium BonFire food, diesel and unleaded fuel, and in-store merchandise. The company is on an expansion spree and as part of its growth, it recently acquired “ Kum & Go” nearly doubling its store count.

### Problem statement:
The company is planning to open 30 new stores yearly in a new market, and it needs to forecast daily sales for the new store. This is crucial for financial planning and return on investment (ROI) assessment for these new stores. The challenge lies in predicting the first-year sales for these newly acquired stores accurately.

We have limited amount of data; therefore, We will be using currently available historical dataset to address analytical problems We will be addressing in this project are identifying trends and patterns in sales data, understanding the relationship between sales and other factors, and identifying outliers and anomalies. By addressing these analytical problems, We will be able to build a sales forecasting model.

### Objective:
To develop a sales forecasting model that can accurately predict daily sales for the new store. We will be using a variety of forecasting methods, such as time series analysis, regression analysis, causal analysis, and machine learning. The model will be evaluated by comparing its prediction to actual sales data from a holdout dataset. The model performance will be evaluated using industry-standard metrics such as Forecast Accuracy Metrics (e.g. MAE, MAPE, RMSE) and its ability to update forecasts dynamically in response to new data.

This sales forecasting model will help the company to make informed decisions about staffing, inventory, and marketing for the new stores. This can help the company to maximize its profits and minimize its losses while maintaining customer satisfaction.

## 2. Solution:



## 3. My Contribution to the Project:

### 3.1 Exploratory Data Analysis:

#### Soft Opening Sales Trends:
Analyzed soft opening dates to discern notable sales patterns during initial operational phases. Day-2 consistently outperformed Day-1 for most stores, indicating positive early engagement. This trend extended to week-2 surpassing week-1 and month-2 exceeding month-1 sales, highlighting a favorable momentum in the initial stages of store operations. These insights guide businesses in optimizing sales strategies during crucial soft opening phases.

#### Seasonal Store Openings and Sales Correlation Analysis:
Explored correlations between store sales and demographic factors, uncovering significant associations. Presence of bonfire_grill and pizza correlated strongly with food service sales, providing strategic direction for product offerings. Positive correlations were identified between employee-to-population ratio and store sales, suggesting advantages for businesses in areas with higher employment density. Examined seasonal trends in store openings, noting higher frequencies in summer and spring and fewer in winter. These findings offer actionable insights for businesses in planning optimal opening periods based on seasonal considerations.

### 3.2 Modelling:

#### Decomposition and Stationarity Analysis:
Conducted a thorough exploration of time series decomposition to identify patterns in sales datasets. Notably, "Total_inside_sales" exhibited a consistent seasonal pattern with higher sales in summer and lower sales in winter. Confirmation of stationarity for all target variables was crucial for subsequent ARIMA and SARIMA modeling, ensuring reliable forecasting.

#### ARIMA Modeling Insights:
Focused on site-21980, applying ARIMA modeling to assess performance based on the "total_inside_sales" target variable. Despite showcasing low MAE at 306.83 and RMSE at 391.75, ARIMA was deemed unsuitable due to limitations. ARIMA failed to account for distinctions between weekdays and weekends, lacked inherent consideration for holidays, and struggled to capture intricate seasonal patterns. These shortcomings prompted exploration of Seasonal ARIMA (SARIMA) models for improved forecasting accuracy.

#### SARIMA Model Evaluation:
Conducted SARIMA modeling on site number 21560, utilizing different training and testing splits. Notable results included a 70:30 split yielding the lowest RMSE and second lowest MAE, establishing it as the optimal model choice. However, SARIMA models, akin to ARIMA, faced challenges in accurately forecasting sales patterns concerning weekly seasonality, weekend versus weekday sales, and holiday versus non-holiday sales. Limitations notwithstanding, the SARIMA model selection process and outcomes are documented, providing valuable insights into time series forecasting for sales data.

## 4. The Business Value of the Solution:



## 5. Difficulties faced:



## 6. My Learnings:




