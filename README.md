# Customer Analytics and Experimental Test

## Project Background
This is the Quantium Data Analytics project from Forage. The client wants to better understand the types of customers who purchase Chips and their purchasing behaviour within the region. And  then test the impact of the new trial layouts with a data driven recommendation to whether or not the trial layout should be rolled out to all their stores. The [interactive dashboard](https://public.tableau.com/app/profile/jia.xu4667/viz/quantium_project_report/Dashboard1) could be found here.


[![Dashboard-image.png](https://i.postimg.cc/MTCdzW8C/Dashboard-image.png)](https://postimg.cc/7GNgVrh9)


## North Star Metrics and Dimensions
1. number of sales
2. number of revenue
3. number of customer
4. unit price per Customer
5. unit per Customer
6. Store Type: Trial or Control 

## Summary of Insights

**Overall Sales Trend**: 
- The number of chip sales has remained relatively consistent over the last one year from July 2018 July to July 2019; a noticebale increase occured in the week leading up to the Christmas.

**Customer segmentation**:
- Older and Young Family shoppers purchase the highest avg units per transaction, indicative of impulsive buying behavior.
- Sales have primarily been driven by three customer segments: Budget - older families, Mainstream - young singles/couples, and Mainstream - retirees shoppers. The notable increase in chip spending for these segments is attributed to their larger population compared to other buyer groups.
- A particularly noteworthy insight is that Mainstream - young singles and couples are 23% more likely to purchase Tyrrells chips than the rest of the population.
- The Category Manager may consider strategically placing Tyrrells and smaller chip packs in discretionary spaces frequented by young singles and couples. 

**Experimental Test**: 

- The control store is constructed to reflect performance of the trial store rather than the average of other stores; from Feb to May the trial store outperformed the control store highlighting the success of the new store layout

  
## Data Overview 
There are three datasets inculding "QVI_purchase_behaviour.csv" & "QVI_transaction_data.csv" for EDA, "QVI_data.csv" for TEST. 

## Notebooks Overview
**1. (EDA) Data prep and customer analytics.ipynb**

**Purpose**: This notebook focuses on Exploratory Data Analysis (EDA) and data preparation steps to understand customer behavior and prepare the data for further analysis.

**Key Steps**:

* **Data Loading**: Load the dataset and necessary libraries.
* **Data Cleaning**: Handle missing values, correct data types, and filter out irrelevant data.
* **Feature Engineering**: Create new features that can help in understanding customer behavior better.
* **Descriptive Statistics**: Compute summary statistics to get an overview of the data.
* **Visualization**: Use various plots to visualize the distribution and relationships within the data.

**2. (TEST) Experimentation and uplift testing copy.ipynb**
**Purpose**:This notebook is dedicated to experimentation, specifically conducting A/B tests to evaluate the impact of certain interventions (e.g., marketing campaigns) on sales and other metrics.

**Key Functions**:
**monthly_measure_metric()**:
* Aggregates monthly sales metrics for each store.
* Computes additional metrics like transactions per customer, chips per transaction, and average price per unit.
* Returns a DataFrame with the aggregated metrics.

**get_test(trial_num, column)**:
* Conducts an A/B test for a given trial store number and metric.
* Computes the ratio of control to trial metrics for pre-trial periods.
* Scales control store metrics to match the trial store for comparison.
* Calculates percentage differences and t-values for post-trial periods.
* Returns standard deviation of pre-trial percentage differences, t-values for post-trial periods, and the critical t-value for significance testing.
