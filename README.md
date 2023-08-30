# Customer-Segmentation

# Use Case
#### Use Case Summary
#### Objective Statement:
- To analyze the monthly and yearly grand totals to identify trends and patterns.
- To segment customers using the RFM model to identify high-value customers.
- To develop marketing strategies to target high-value customers and increase revenue.

#### Challenges:
- The dataset is large and has different data types.
- It is difficult to get the frequency of customer purchases using the Groupby method.

#### Methodology / Analytic Technique:
- Exploratory data analysis (EDA) will be used to identify trends and patterns in the data.
- A clustering model will be used to segment customers into different groups based on the RFM model.
- Segment analysis will be used to develop marketing strategies to target high-value customers.

#### Business Benefit:
- The business will be able to better understand its customers and their needs.
- The business will be able to develop more effective marketing strategies to target high-value customers.
- The business will be able to increase revenue by targeting high-value customers.

#### Expected Outcome:
- The business will know the grand total in each year.
- The business will know the grand total per month in each year and the month with the highest and lowest grand total in each year.
- The business will know the comparison of the grand total between each year and the month with the most significant decrease and increase in each year.
- The business will be able to segment customers using the RFM model.
- The business will know how to optimize marketing strategies to the right customers to generate more revenue.

# Business Understanding
Retail is the process of selling consumer goods or services to customers through multiple channels of distribution to earn a profit. In this case, we are interested in understanding the monthly and yearly grand totals of a retail business. We also want to segment customers using the RFM model and develop marketing strategies to target high-value customers.

This case requires data-driven answers to the following questions:
- How much is the grand total in each year? (This question will help us to understand the overall sales of the retail business over time.)
- How much is the grand total per month in each year and which month has the highest and lowest grand total in each year? (This question will help us to identify the months that are typically the busiest and slowest for the retail business.)
- How is the comparison of the grand total between each year and which month has the most significant decrease and increase in each year? (This question will help us to understand how the retail business is performing over time and which months are seeing the most significant changes in sales.)
- How is the customer segmentation using RFM model? (This question will help us to identify different groups of customers based on their recency, frequency, and monetary value.)
- How to optimize marketing strategies to the right customers to generate more revenue? (This question will help us to develop marketing strategies that are targeted to high-value customers.)

# Data Understanding
* The data set contains information about retail transactions from 4 January 2011 to 31 December 2014.
* The dataset has 4 columns and 5009 rows.

#### Data Source
* Source Data: https://www.kaggle.com/datasets/siddinho/sample-orders-dataset-retail    

#### Data Dictionary 
* Order Date 	: Transaction date
* Order Id		: Order code of each transaction
* Customer		: Customer's name
* Grand Total	: Total customer spending

# Data Preparation
Code Used :
* Python Version :Python 3.8.8
* Packages : Pandas, Numpy, Matplotlib, Seaborn, SKlearn,  Datetime, Plotly, Feature Engine, Warnings

# Data Cleansing
* We need to change the order_date data type from object to datetime because the column value is a transaction date which should be a datetime data type.
* We need to create a new column that takes only the year and month from order_date column

# Exploratory Data Analysis

#### How much is the grand total per month in each year and which month has the highest and lowest grand total in each year?
- 2011
![image](https://user-images.githubusercontent.com/83635356/201461115-e82dc6e4-4112-4902-adcb-3ee07a016d01.png)

The graph shows the total sales for each month of the year 2011. **February had the lowest total sales of 1%**, while **September had the highest total sales of 16.9%**.

There were a few significant changes in total sales throughout the year. From January to February, there was a decrease of 1.9%. From February to March, there was a significant increase of 10.5%. From March to April, there was a decrease of 5.7%. From April to August, there was no significant change in total sales. From August to September, there was an increase of 11.1%. From September to October, there was a large decrease of 10%. From October to November, there was an increase of 9.7%. And in November, the total sales for the year closed at 14.4%.

**September was the month that experienced the biggest increase in total sales of 11.1%**. **October was the month that experienced the biggest decrease in total sales of 10.4%**.

![image](https://user-images.githubusercontent.com/83635356/201461269-3bd6733f-cafe-4d11-835b-01ddc8a08f39.png)
- 2012
The graph shows the grand total for each month of the year 2012. **February had the lowest grand total of 2.6%**, while **November had the highest grand total of 16.1%**.

There were a few significant changes in grand total throughout the year. In January 2012, the grand total was higher than in January 2011 to 3.9%. February had the lowest grand total of 2.6%. March experienced a significant increase to 8.2%, and April had a slight decrease to 7.3%. May and June had further decreases to 6.4% and 5.3%, respectively. In July, the grand total increased again to 6.1%. August had an increase to 7.8%, and September had a significant increase to 13.7%. October had a significant decrease to 6.7%. The end of the year had very high grand totals, with November at 16.1% and December at 15.9%.

**October was the month that experienced the biggest increase in grand total of 9.4%**, from 6.7% in September to 16.1% in October. **October was also the month that experienced the biggest decrease in grand total of 7%**, from 13.7% in September to 6.7% in October.

- 2013
![image](https://user-images.githubusercontent.com/83635356/201461291-7dd3e285-cca2-40c6-a129-223b7a5ad9b9.png)

The graph shows the grand total for each month of the year 2013. **January had the lowest grand total of 3%**, while **December had the highest grand total of 16%**.

There were a few significant changes in grand total throughout the year. January started with a relatively low grand total of 3%. In February, it increased to 3.8%, and in March it increased to 8.4%. April had a decrease to 6.5%, and May had an increase to 9.3%. June had a decrease to 6.5%. The highest grand total in the first half of the year was in May with 9.3%.

Entering the second half of 2013, the grand total for July and August did not differ significantly, with 6.3% and 5.5%, respectively. In September, there was a significant increase in the grand total of up to 12%. Sales tend to increase at the end of the year, with 14% in November and 16% in December.

**September was the month that experienced the biggest increase in grand total of 6.5%**, from 5.5% in August to 12% in September. **June was the month that experienced the biggest decrease in grand total of 2.8%**, from 9.3% in May to 6.5% in June.

- 2014
![image](https://user-images.githubusercontent.com/83635356/201461338-64f5a67a-6aae-4763-8f16-102ac03e6761.png)

The graph shows the grand total for each month of the year 2014. **February had the lowest grand total of 2.8%**, while **November had the highest grand total of 15.3%**.

There were a few significant changes in grand total throughout the year. January started with a grand total of 6.1%, which was higher than the previous year. February had a decrease to 2.8%, and March had a significant increase to 7.3%. April had a gradual increase in grand total to 5.5%, followed by a further increase to 6.2% in May and 6.6% in June. The grand total was stagnant at 6.6% from June to July. August had an increase in grand total to 8.4%, followed by an increase to 12.3% in September. October had a decrease in grand total to 10.6%, before November had a significant increase to 15.3%. December had a decrease in grand total to 12.3%.

**November was the month that experienced the largest increase in grand total of 4.7%**, from 10.6% in October to 15.3% in November. **February was the month that experienced the biggest decrease in grand total of 3.3%**, from 6.1% in January to 2.8% in February.

#### How much is the grand total in each year?

![image](https://user-images.githubusercontent.com/83635356/201461798-ef84b67d-2d85-471f-8be0-1cd285d2d5f0.png)

The chart shows the grand total for each year. **The lowest grand total was in 2012 at 20.5%**, while **the highest grand total was in 2014 at 32%**.

There was a decrease in total sales in 2012 from 0.6% in 2011. However, there was an increase in total sales in 2013 and 2014.

In 2011, the grand total was 21%. In 2012, total sales decreased by 0.6% to 20%. In 2013, the grand total increased by 5.1% to 26.5%. In 2014, the grand total increased by 5.5% to 32%.

#### How is the comparison of the grand total between each year and which month has the most significant decrease and increase in each year?


![image](https://user-images.githubusercontent.com/83635356/201462304-257e2172-41a1-411f-8aa0-056699bcd5ab.png)

The graph shows the total monthly income for each year. **2014 had the highest total income every month**. There are several patterns that are similar in each year:

* From February to March, there is an increase in total income.
* From August to September, there is also an increase in total income, but from September to October, there is a decrease.
* In October to November, there is an increase in total income.
* It is estimated that the increase in total income in November is due to the Black Friday event, which is held every year.

The green line (2013) is slightly different from the other years at the beginning and end of the year. In 2013, there was an increase in income from January to February, and from October to December.

# Preprocessing Modeling
# RFM Analysis

RFM analysis is basically scoring our customers based on their Recency, Frequency and Monetary values.
- Recency : How long it’s been since a customer bought something from us.
- Frequency : How often a customer buys from us.
- Monetary : The total value of purchases a customer has made

# Modeling Data : RFM Quantiles
To score each column of Recency, Frequency, and Monetary, we first determine a score range from 1 to 4. The highest score is 1 and the lowest score is 4.

* Recency: This column measures how recently a customer has made a purchase. A score of 1 means the customer has made a purchase recently, and a score of 4 means the customer has not made a purchase in a long time.
* Frequency: This column measures how often a customer makes purchases. A score of 1 means the customer makes purchases very often, and a score of 4 means the customer makes purchases very rarely.
* Monetary: This column measures the total amount of money a customer has spent. A score of 1 means the customer has spent a lot of money, and a score of 4 means the customer has spent very little money.

Once we have determined the score range for each column, we can assign a score to each customer. The score for each column is determined by comparing the customer's value in that column to the quantiles of the column. The quantiles are the values that divide the column into four equal parts.

# Label

Based on the RFM data the customer is labeled into 6 parts. for details:
- If the **RFM_Segment is 111** then the customer labeled as **Best Customers**.
- If the **F_quartile is 1** then the customer labeled as **Loyal Customers**.
- If the **M_quartile is 1** then the customer labeled as **Big Spenders**.
- If the **RFM_Segment is 134** then the customer labeled as **Almost Lost**.
- If the **RFM_Segment is 344** then the customer labeled as **Lost Customers**.
- If the **RFM_Segment is 444** then the customer labeled as **Lost Cheap Customers**.

#### How is the customer segmentation using RFM model?

![image](https://user-images.githubusercontent.com/83635356/201461741-c91d323d-cc2b-4690-abd6-f42dc69ee102.png)

The chart shows the results of customer clustering, which is a process of grouping customers together based on their RFM (Recency, Frequency, Monetary) scores. The RFM scores are calculated based on how recently a customer has made a purchase, how often they make purchases, and how much money they spend.

The chart shows that the customers have been clustered into 6 categories:

* Loyal Customers: These customers make frequent purchases and have a large monetary value. They represent 33.6% of all customers.
* Big Spenders: These customers have a large monetary value, but they may not make purchases very often. They represent 32.6% of all customers.
* Lost Cheap Customers: These customers have not made a purchase in a long time, they rarely make purchases, and they do not have a large monetary value. They represent 17.4% of all customers.
* Lost Customers: These customers have not made a purchase in a long time, they rarely make purchases, and they have a low monetary value. They represent 8.1% of all customers.
* Best Customers: These customers have recently made a purchase, they make frequent purchases, and they have a large monetary value. They represent 7.8% of all customers.
* Almost Lost: These customers have recently made a purchase, they make purchases quite often, but they have a low monetary value. They represent 0.5% of all customers.

The remaining 52% of customers do not fit into any of these categories and are labeled as "Others."

# Result

- In 2011, **February had the lowest total sales of 1%**, while **September had the highest total sales of 16.9%**. **September was the month that experienced the biggest increase in total sales of 11.1%**. **October was the month that experienced the biggest decrease in total sales of 10.4%**.


- In 2012, **February had the lowest grand total of 2.6%**, while **November had the highest grand total of 16.1%**. **October was the month that experienced the biggest increase in grand total of 9.4%**, from 6.7% in September to 16.1% in October. **October was also the month that experienced the biggest decrease in grand total of 7%**, from 13.7% in September to 6.7% in October.


- In 2013, **January had the lowest grand total of 3%**, while **December had the highest grand total of 16%**. **September was the month that experienced the biggest increase in grand total of 6.5%**, from 5.5% in August to 12% in September. **June was the month that experienced the biggest decrease in grand total of 2.8%**, from 9.3% in May to 6.5% in June.


- In 2014, **February had the lowest grand total of 2.8%**, while **November had the highest grand total of 15.3%**. **November was the month that experienced the largest increase in grand total of 4.7%**, from 10.6% in October to 15.3% in November. **February was the month that experienced the biggest decrease in grand total of 3.3%**, from 6.1% in January to 2.8% in February.


The model was also able to identify 4 trends in the monthly income data:

- February to March: There is an increase in total income from February to March in each year.


- August to September: There is also an increase in total income from August to September, but from September to October, there is a decrease.


- October to November: In October to November, there is an increase in total income.


- Lowest and Highest Grand Total: The lowest grand total was in 2012 at 20.5%, while the highest grand total was in 2014 at 32%.

The customer segments are:

- Loyal Customers: These customers make frequent purchases and have a large monetary value. They represent 33.6% of all customers.


- Big Spenders: These customers have a large monetary value, but they may not make purchases very often. They represent 32.6% of all customers.


- Lost Cheap Customers: These customers have not made a purchase in a long time, they rarely make purchases, and they do not have a large monetary value. They represent 17.4% of all customers.


- Lost Customers: These customers have not made a purchase in a long time, they rarely make purchases, and they have a low monetary value. They represent 8.1% of all customers.


- Best Customers: These customers have recently made a purchase, they make frequent purchases, and they have a large monetary value. They represent 7.8% of all customers.


- Almost Lost: These customers have recently made a purchase, they make purchases quite often, but they have a low monetary value. They represent 0.5% of all customers.

# Recommendation
- Target marketing campaigns to specific customer segments: A business could target "Loyal Customers" with promotional offers for their products or services. This could include discounts, free shipping, or early access to new products. The business could also target "Almost Lost" customers with loyalty programs that offer rewards for making repeat purchases, as these customers are likely to churn.


- Monitor trends in monthly income. Businesses can monitor the trends in monthly income identified by the model to track the performance of their marketing campaigns. For example, businesses can look for increases in total income from February to March, as this may indicate that their marketing campaigns are effective in increasing sales.


- Make adjustments to marketing campaigns as needed. Businesses can make adjustments to their marketing campaigns as needed based on the findings of the machine learning model. For example, businesses might increase the frequency of their promotional offers to "Loyal Customers" if they see that these customers are responding well to the offers. Businesses might also decrease the frequency of their marketing campaigns to "Almost Lost" customers if they see that these customers are not responding well to the campaigns.
