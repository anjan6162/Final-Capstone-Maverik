# Maverik Sales Forecasting

## 1. Business Problem Statement:

Maverik, a retail convenience chain with over 380 locations across 12 western states, is expanding rapidly. Recently, it doubled its store count by acquiring 'Kum & Go.' The company aims to open 30 new stores yearly in a new market and needs to accurately predict daily sales for these new stores. This is crucial for financial planning and assessing return on investment. Our goal is to analyze the available historical data, identify trends and patterns in sales, understand the relationship between sales and other factors, and detect outliers and anomalies. Through this analysis, we aim to develop a reliable sales forecasting model to support Maverik's expansion plans.

## 2. Our Solution:

We created a sales forecasting model to accurately predict daily sales for the new store over any given number of days from its opening. Utilizing diverse forecasting methods including XGB, Prophet, ARIMA/SARIMA, and ETS, we rigorously assessed model performance by comparing predictions against actual sales data from a holdout dataset. Our evaluation, aligned with Maverick's benchmark indices, showcased excellent results. Each model underwent scrutiny using industry-standard metrics like MAE, MAPE, and RMSE, ensuring robust accuracy and the ability to dynamically update forecasts with new data.

## 3. My Contribution to the Project:

### 3.1. Exploratory Data Analysis:

#### Soft Opening Sales Trends:
Analyzed soft opening dates to discern notable sales patterns during initial operational phases. Day-2 consistently outperformed Day-1 for most stores, indicating positive early engagement. This trend extended to week-2 surpassing week-1 and month-2 exceeding month-1 sales, highlighting a favorable momentum in the initial stages of store operations. These insights guide businesses in optimizing sales strategies during crucial soft opening phases.

#### Seasonal Store Openings and Sales Correlation Analysis:
Explored correlations between store sales and demographic factors, uncovering significant associations. Presence of bonfire_grill and pizza correlated strongly with food service sales, providing strategic direction for product offerings. Positive correlations were identified between employee-to-population ratio and store sales, suggesting advantages for businesses in areas with higher employment density. Examined seasonal trends in store openings, noting higher frequencies in summer and spring and fewer in winter. These findings offer actionable insights for businesses in planning optimal opening periods based on seasonal considerations.

### 3.2. Modelling:

#### Decomposition and Stationarity Analysis:
Conducted a thorough exploration of time series decomposition to identify patterns in sales datasets. Notably, "Total_inside_sales" exhibited a consistent seasonal pattern with higher sales in summer and lower sales in winter. Confirmation of stationarity for all target variables was crucial for subsequent ARIMA and SARIMA modeling, ensuring reliable forecasting.

#### ARIMA Modeling Insights:
Focused on site-21980, applying ARIMA modeling to assess performance based on the "total_inside_sales" target variable. Despite showcasing low MAE at 306.83 and RMSE at 391.75, ARIMA was deemed unsuitable due to limitations. ARIMA failed to account for distinctions between weekdays and weekends, lacked inherent consideration for holidays, and struggled to capture intricate seasonal patterns. These shortcomings prompted exploration of Seasonal ARIMA (SARIMA) models for improved forecasting accuracy.

#### SARIMA Model Evaluation:
Conducted SARIMA modeling on site number 21560, utilizing different training and testing splits. Notable results included a 70:30 split yielding the lowest RMSE and second lowest MAE, establishing it as the optimal model choice. However, SARIMA models, akin to ARIMA, faced challenges in accurately forecasting sales patterns concerning weekly seasonality, weekend versus weekday sales, and holiday versus non-holiday sales. Limitations notwithstanding, the SARIMA model selection process and outcomes are documented, providing valuable insights into time series forecasting for sales data.

## 4. The Business Value of the Solution:

Our forecasting solution provides significant benefits for Maverik, enabling efficient resource allocation, optimization of staffing and inventory management, and informed decision-making in marketing and promotions. Through the creation of accurate financial plans and ROI documents, Maverik can confidently assess the return on investments in new stores, fostering a more strategic and well-informed approach to expansion.

## 5. Difficulties faced:

### 5.1. Extended Model Run Times: 
The modeling phase, particularly in SARIMA, presented challenges with extended run times. Attempting to achieve daily granularity (s=365) in SARIMA, which would have provided a more detailed understanding of the daily sales patterns, resulted in impractical run times due to technical constraints. Striking a balance between detailed granularity and computational efficiency became a key challenge in achieving the desired precision in time series forecasting.

### 5.2. Complexity in Capturing Seasonal Patterns: 
Both ARIMA and SARIMA models struggled to capture complex sales patterns, especially concerning seasonality and holiday-specific variations. The inherent limitations of these models in handling intricate temporal trends posed a challenge in accurately forecasting sales data, necessitating a careful consideration of alternative approaches and model refinement to enhance predictive capabilities.

### 5.3. Optimal Model Selection: 
Choosing the optimal model for forecasting, especially when considering various factors such as seasonality, holidays, and week-specific sales trends, posed inherent difficulties. The diverse characteristics of the Maverik sales data required meticulous evaluation and comparison of different forecasting methods, emphasizing the ongoing challenge of balancing model complexity and accuracy to meet Maverik's specific business objectives.

These difficulties underscore the intricate nature of time series forecasting in the retail domain and highlight the ongoing need for a nuanced approach to modeling, considering computational constraints, seasonal intricacies, and the diversity of sales patterns across different product categories.

## 6. My Learnings:

Throughout this project, I deepened my understanding of time series forecasting, particularly in the context of Maverik's expansion strategy. The core challenge of predicting daily sales for new stores highlighted the critical role of accurate forecasting in financial planning and ROI assessment for businesses.

### 6.1. Business Problem Understanding:
Navigating Maverik's expansion plan underscored the pivotal importance of time series forecasting for guiding strategic decisions. The practical implications of forecasting daily sales for financial planning and ROI assessment became evident, emphasizing the direct impact on business sustainability and growth.

### 6.2. Data Exploration and Analysis:
Conducting exploratory data analysis (EDA) revealed insights into time series patterns, crucial for understanding sales dynamics. Uncovering correlations between various factors and sales further emphasized the nuanced nature of time-dependent data, showcasing the need for robust forecasting models.

### 6.3. Modeling Solutions:
The modeling phase brought to light challenges in traditional time series approaches such as ARIMA and SARIMA. Leveraging advanced techniques like XGBoosting proved essential for addressing the complexities inherent in time series data. This experience emphasized the practical application of time series forecasting methods, reinforcing their significance in deriving meaningful insights from historical sales data.
