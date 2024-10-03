# JDE-Final-Project

# INTRODUCTION
The Brazilian Olist E-Commerce Dataset is a comprehensive dataset provided by Olist, a marketplace platform in Brazil. This dataset is highly valuable for exploring various aspects of e-commerce transactions, customer behaviors, seller performance and delivery in the Brazilian market.This dataset contains 100,000 records across various marketplaces  for orders recorded between 2016-2018. 

# Potential Use Cases
Customer Segmentation
- Identify valuable customers based on purchase behavior
Sales Performance Analysis
- Analyze top product categories and seller performance
Delivery Performance
- Assess average delivery times and delays across regions
Customer Satisfaction
- Use customer reviews to understand satisfaction levels
Payment Behavior Analysis
- Investigate payment methods and installment behaviors
Delivery Pipeline Analysis
- Identify problems in pipeline to efficiently carry out delivery process

# ETL - Microsoft Azure
![image](https://github.com/user-attachments/assets/025fb016-d776-4de6-92bb-f25158c57373)

My group decided to utilize Microsoft Azure services for our ETL project. We first created storage containers to pull the data from github and store. The data was in csv format.
After which, we mounted the container onto DataBricks platform so that we will be able to access the files for data transformation.
In DataBricks, we used pySpark to clean the data and get it ready for analysis. After transformation, we returned the cleaned files into a data lake as a parquet file. 
Why parquet files? Parquet's columnar storage and efficient compression makes it well-suited for analytical queries that only need to access specific columns.

After which, we will be able to query the data using Microsoft Synapse Analytics if we want some quick answers from the data. We also were able to connect the data to Power BI for our visualizations
for insights.


# Entity Relationship Diagram
![image](https://github.com/user-attachments/assets/2029575c-fc7b-4132-9bb3-a519044b5b5e)


# Problem Statement
- Analyze the Olist e-commerce dataset to identify key factors affecting customer satisfaction, sales performance, and operational efficiency. 
- Provide actionable insights to optimize customer experience, streamline order processing, and improve overall profitability."

# Operations Analysis
![image](https://github.com/user-attachments/assets/18912f52-f2f3-4a63-8aa2-aade24c1adf5)

# Insights
There is an increasing sales from February 2017 to Q2 of financial year 2018
- Actionable Insight: Dig into the sales product categories, identify contributing items

Relative to weekdays, weekends tend to bring in more sales volume. Credit card was found to be the most preferred payment type
- Actionable Insight: Analyze probable reasons as to why credit card was most preferred. May be due to promotions, cash-back offerings etc.

Linear correlation: Higher review score associated with lower number of shipping days. Another point to consider is the condition of shipped items when the customers receive. The higher review score may also be attributed by excellent state of items upon receipt.

# Sales Performance

[PowerBI](https://app.powerbi.com/links/C2HQ0Kro-H?ctid=0d5e4a9c-7c9a-4b3f-ae60-6fe77a9e77e4&pbi_source=storytelling_addin)
