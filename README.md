# Rossmann Store Sales Project Overview

## Background

Rossmann, Germany's largest grocery store chain, operates over 3000 stores across 7 European countries. Sales are influenced by various factors including promotions, competition, and holidays.

## Data Presentation

The dataset comprises data from 1115 stores, totaling 1,017,209 entries with 27 attributes, recorded from January 2013 to July 2015. It includes:

- train.csv: historical data with sales volume
- test.csv: historical data without sales
- sample_submission.csv: a sample file submitted in the correct format
- store.csv: some additional information about each store

Train.csv contains a total of 9 columns of information:
- store: is the id number of the corresponding store
- DayOfWeek: represents the number of days per week that the store is open
- Data: is the date when the corresponding sales were generated
- Sales: is the historical data of sales
- Customers: is the number of customers who came into the store
- Open: indicates whether the store is open or not
- Promo: indicates whether the store has a promotion on that day
- StateHoliday: and SchoolHoliday indicate whether it is a national holiday or a school holiday, respectively.

Store.csv contains the following information:
- Store: Identifies the store number.
- StoreType: Defines the store's category, with four distinct classifications: a, b, c, and d. These could represent various retail formats such as flash sales outlets, general retailers, flagship stores, or small-scale shops, akin to the diverse retail experiences we encounter.
- Assortment: Uses a, b, and c to denote the product range's breadth available in the store, highlighting the variation in product selections from one store type to another, like between flagship and mini stores.
- Competition Distance, Competition Open Since Year, Competition Open Since Month: These fields specify the proximity to the closest competing store, and the year and month since that competitor was established, respectively.
- Promo2: Indicates the presence of a long-term promotional strategy within the store.
- Promo2 Since Year, Promo2 Since Week: These detail the specific year and week when the store commenced its involvement in the long-term promotional activities.
- Promo Interval: Outlines the periodicity of the Promo2 campaign, named for the months when the promotion is reinitiated.


## Project Objectives

Utilize historical sales data (`train.csv`) for supervised learning to predict future sales, which are submitted to Kaggle.

## Evaluation Criteria

The model's performance is evaluated using the Root Mean Square Percentage Error (RMSPE), focusing on accuracy in sales prediction.

### Calculation for RMSPE

The Root Mean Square Percentage Error (RMSPE) is calculated using the formula:

$$
RMSPE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} \left(\frac{y_i - \hat{y}_i}{y_i}\right)^2}
$$

## Project Process

1. **Loading Data**: Understanding the various information dimensions available.
2. **EDA (Exploratory Data Analysis)**: Using tools like Pandas, Matplotlib, and Seaborn for data visualization.
3. **Data Pre-processing**: Addressing missing values through removal, filling, or marking.
4. **Feature Engineering**: Extracting time-related features and converting categorical data into numerical format.
5. **Benchmark Model and Evaluation**: Establishing a baseline model and defining an evaluation criterion based on RMSPE.
6. **XGBoost Modeling**: Adjusting parameters of the XGBoost model to improve prediction accuracy.

## Model Parameters

- **eta**: Learning rate.
- **max_depth**: Maximum depth of a tree.
- **subsample**: Sampling ratio for training data.
- **colsample_bytree**: Sampling ratio for features.
- **num_round**: Number of trees.

Please note that specific model tuning techniques like GridSearchCV are not in the code as per the project requirements.





