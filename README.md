# Data Preparation, Customer Analytics, and Experimentation

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
