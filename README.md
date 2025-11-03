# MSCS_634_ProjectDeliverable_1
This repository contains the Project 1 deliverable, focusing on the data collection, cleaning, and exploratory data analysis (EDA) of a retail sales dataset.

Dataset Summary & Key Insights

Dataset Summary: 
This project uses a Retail Sales Dataset containing 1,000 transaction records with nine attributes, including customer demographics, product details, and purchase amounts. It's a well-structured dataset suitable for exploring customer behavior and sales trends.


Key Insights from Analysis:
Sales Distribution is Uneven: Most sales are for moderate amounts, but a few high-value transactions contribute significantly to total revenue. This is a common pattern in retail, resembling a Pareto-like distribution.


Demographics are Balanced: Sales are split almost equally between male and female customers and across the three product categories (Clothing, Electronics, and Beauty). This suggests a broad customer base.


Key Correlations: As expected, the Total Amount of a sale is strongly and positively correlated with the Price per Unit and moderately correlated with the Quantity of items purchased.

Major Steps in Data Cleaning and Exploration
Data Loading and Inspection: The dataset was first loaded into a pandas DataFrame. Initial checks were performed using .info() and .describe() to understand its structure, identify data types, and check for missing values.


Data Cleaning:

Duplicate Removal: The dataset was checked for any duplicate rows to prevent bias in the analysis, and none were found.

Data Type Conversion: The Date column was converted from a text/object format to a proper datetime object, which is essential for performing any time-series analysis.


Exploratory Data Analysis (EDA):

Univariate Analysis: Histograms and count plots were used to visualize the distributions of individual variables like customer age, product categories, and transaction amounts.

Outlier Detection: A boxplot was used to visualize the spread of the Total Amount and identify potential outliers.

Bivariate Analysis: A correlation heatmap and scatterplots were generated to explore relationships between numerical variables.

Challenges and Solutions
Challenge: Incorrect Date Format 🗓️

The transaction dates were initially stored as text strings (e.g., "24/11/2023"), which made it impossible to analyze sales over time.

Solution: This was resolved by using the pandas.to_datetime() function. This converted the entire column into a datetime object, enabling chronological sorting and time-series plotting.

Challenge: Interpreting Outliers 📈

The EDA revealed potential outliers, especially in the Total Amount. A key decision was whether these were data errors or valid, high-value purchases.

Solution: After consideration, the outliers were kept in the dataset. They were interpreted as legitimate high-value transactions, which are crucial for a complete business analysis. Removing them would have meant losing valuable information about the most significant sales events.