# Walmart Sales Forecasting
## Business Problem
In this project, the goal is to predict department-wide sales for each of the 45 Walmart stores located in different regions, based on historical sales data. This task is made more complex by the inclusion of selected holiday markdown events, which affect sales unpredictably.

## Data Description
Link: https://www.kaggle.com/datasets/aslanahmedov/walmart-sales-forecast/data

The dataset provided for this project consists of several files:

##### stores.csv: Contains anonymized information about the 45 stores, including the type and size of each store.

##### train.csv: Historical training data from 2010-02-05 to 2012-11-01. Fields include:

Store: the store number

Dept: the department number

Date: the week

Weekly_Sales: sales for the given department in the given store

IsHoliday: whether the week is a special holiday week

##### test.csv: Similar to train.csv, but without the weekly sales data, which you need to predict.

##### features.csv: Contains additional data related to store, department, and regional activity for given dates. Fields include:
Store: the store number

Date: the week

Temperature: average temperature in the region

Fuel_Price: cost of fuel in the region

MarkDown1-5: anonymized data related to promotional markdowns (only available after Nov 2011)

CPI: consumer price index

Unemployment: unemployment rate

IsHoliday: whether the week is a special holiday week


## Project Steps
### 1. Data Loading and Preparation

Import the necessary libraries.

Mount Google Drive and read the data from CSV files.

Merge the train, features, and stores datasets into a single DataFrame.

Perform data cleaning and handle missing values.

### 2. Exploratory Data Analysis (EDA)

Visualize the distribution of stores by type and size.

Analyze the sales data by department and store.

Examine the impact of holidays on weekly sales using bar plots and time series analysis.

Create new features to identify specific holidays (Super Bowl, Labor Day, Thanksgiving, and Christmas).

### 3. Data Preprocessing

Handle missing values by filling them appropriately.

Convert categorical variables into numerical values for modeling.

Normalize the data if necessary.

### 4. Model Building and Evaluation

Split the data into training and testing sets.

Train models using regression algorithms such as Ridge and Lasso.

Perform hyperparameter tuning using GridSearchCV and RandomizedSearchCV.

Evaluate the models using metrics like Mean Squared Error (MSE), Mean Absolute Error (MAE), and R-squared.

### 5. Visualization

Plot the average weekly sales per year to identify trends and patterns.

Visualize the average sales per department and store.

Create correlation matrices to understand relationships between features.

## Results and Insights
During the exploratory data analysis (EDA), several key insights were uncovered:

. Store distribution by type revealed that most stores were of type A, followed by type B and then type C. Type A stores also tended to have the highest sales volume.

. Weekly sales varied significantly across departments, with some departments consistently outperforming others.

. Holidays, especially major ones like Thanksgiving and Christmas, had a noticeable impact on sales, leading to spikes in revenue during those periods.

. New features created to identify specific holidays provided a clearer understanding of how each holiday affected sales differently.

In terms of model performance, both Ridge and Lasso regression models showed good performance in predicting weekly sales. The best-performing model achieved a low Mean Squared Error (MSE) and Mean Absolute Error (MAE), indicating accurate predictions.

## Conclusion
The Walmart Sales Forecasting project successfully addressed the business problem of predicting department-wide sales across 45 stores, considering various factors such as store type, holiday markdowns, and historical sales data. The key takeaways from this project include:

##### . Impact of Holidays: 
Holidays significantly influence sales, and accounting for them in forecasting models is crucial for accurate predictions.

##### . Model Performance: 
Both Ridge and Lasso regression models showed strong performance, highlighting their suitability for sales forecasting tasks.

##### . Data Insights: 
EDA revealed insights into store distribution, departmental sales variations, and the effects of holidays on sales patterns.

Moving forward, potential improvements and future work could include:

. Incorporating additional external factors like competitor data, economic indicators, and weather conditions for more robust models.

. Experimenting with advanced modeling techniques such as ensemble methods, neural networks, or time series forecasting models to capture complex sales trends.

Overall, this project provides valuable insights and models that can help Walmart make informed decisions, optimize inventory management, and improve sales forecasting accuracy.
