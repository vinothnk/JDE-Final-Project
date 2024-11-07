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

The snowflake schema consists of one fact table that is connected to many dimension tables, which can be connected to other dimension tables through a many-to-one relationship.
In our ER diagram, the orders table is the primary fact table where other tables are connected to.


# Problem Statement
- Analyze the Olist e-commerce dataset to identify key factors affecting customer satisfaction, sales performance, and operational efficiency. 
- Provide actionable insights to optimize customer experience, streamline order processing, and improve overall profitability."

# OPERATIONS ANALYSIS
![image](https://github.com/user-attachments/assets/18912f52-f2f3-4a63-8aa2-aade24c1adf5)

# Insights
There is an increasing sales from February 2017 to Q2 of financial year 2018
- Actionable Insight: Dig into the sales product categories, identify contributing items

Relative to weekdays, weekends tend to bring in more sales volume. Credit card was found to be the most preferred payment type
- Actionable Insight: Analyze probable reasons as to why credit card was most preferred. May be due to promotions, cash-back offerings etc.

Linear correlation: Higher review score associated with lower number of shipping days. Another point to consider is the condition of shipped items when the customers receive. The higher review score may also be attributed by excellent state of items upon receipt.

# SALES ANALYSIS

![image](https://github.com/user-attachments/assets/b75c88ed-7cd8-410c-b903-d7eb041b1047)

# Insights
Geographical Sales Distribution:​​
- Have identified  bottom 10 revenue generating states contributing to 3.2% of the total sales. Some potential reasons for low sales could be the population size, economic condition, unemployment, limited access to e-commerce platforms​
  - Action: Focus advertising and marketing efforts in regions with lower sales to increase market penetration. Consider adjusting pricing, promotions, or shipping policies based on regional demand and competition.​​

Sales Trends Over Time​:​
- Sales tend to peak in Q2 but seem to dip at the end of Q3 …Reason? ​
  - Action: Align marketing campaigns and inventory planning with peak sales periods. Introduce promotions or discounts during slower sales months to boost revenue.​​

Customer Segmentation:​​
- Customers are segmented according to their purchase history into ‘Very Frequent’ , ‘Frequent’ , ‘Moderate’ and ‘Occasional’​​
  - Action: Tailor marketing strategies for each customer segment. Offer loyalty programs or exclusive discounts for ‘Very Frequent’ and ‘Frequent’ customers​. Re-engage with ‘Moderate’ and ‘Occasional’ customers     
    through personalized offers or follow-up communication.​​

​Top Categories By Revenue and Average Order Value:​​
- These bar charts show top ten categories by revenue. And average order value​
  - Action: Prioritize stocking and promoting these products. Invest in marketing campaigns tailored to these top categories to boost sales further​

​Low-Performing Products:​​
- The Price Vs Freight matrix highlights products whose freight cost is more than the actual cost of the products​​
  - Action: Consider discontinuing such products or exploring ways to reduce shipping costs to increase profit margins.​


# CUSTOMER SATISFACTION & ORDERS ANALYSIS​

![image](https://github.com/user-attachments/assets/7bf9ab19-0c3c-42a7-9d6b-2e28f0b7d922)

There is a direct relationship between Review and delay in delivery. Customers are generally happier when the products are delivered on time.​
  - 4.62 % of orders (5.21K Orders) are delivered out of time. 95.38% Orders are delivered within the estimated time​
  - 26.25% of sellers have at least delayed one order this has direct implication on the product review. ​
- Proposed Action: Find what is causing the delay in delivery ​

​Only 0.63 % of total orders are cancelled and that is not significant when compared to the volume of orders. ​
  - Customers are less likely to cancel the orders once it is placed which shows high customer satisfaction  when it comes to OLIST.​

Close to 75% of orders are coming from three Cities ,Sao Paulo , Rio De Janeiro and Minas Gerais​
  - Sao Paulo , Rio De Janeiro and Minas Gerais  are the top three richest and populous states in Brazil). ​
  - While RJ and MG have almost same number of orders, delay in delivery is higher in RJ. ​
- Proposed Action: Analyse the cause of delay in order delivery to RJ. Also devise strategies to reach out to more customers in other cities, by conducting sales, 
                   offering promotions etc. as there are other similar cities like  RJ and MG in Brazil in terms of population ​


# ORDERS PIPELINE ANALYSIS

![image](https://github.com/user-attachments/assets/2bc041e2-1873-41ba-bbe5-a6014a23d52f)

# Time taken from warehouse to logistics partner
- On average, higher score given due to earlier delivery date compared to estimated date​.
    - review score 1 took 4.16 days to deliver ​
    - review score 5 took 2.37 days to deliver ​

 - Recommendations: ​
   - Optimize warehouse layout to minimize travel time.​
     - identify which specific product categories are frequently ordered and place them together​
   - Implement batch picking or zone picking​
     - batch picking: collecting all required items for multiple orders​
     - zone picking: pickers only pick items within their assigned zone​
​
# Items Count
- No of items to deliver with review score 5 = 2940​
- No of items with review score 1 = 6279​

- Type of items with review score 1 were small appliances, computer accessories, garden tools.​

# Recommendations: ​
- Last mile delivery improvements​
- crowdsource delivery partners for smaller items​
- partner with order fulfillment partner to increase efficiency​
- automate delivery notification​


# CHALLENGES
​- Attribute error issue when using VS Code IDE​
- iterrows & insert method to populate tables on Postgresql​
- Should use df.to_sql method to reduce runtime​
​- Mounting storage container onto Databricks​
- Permission challenges creating Azure accounts​
