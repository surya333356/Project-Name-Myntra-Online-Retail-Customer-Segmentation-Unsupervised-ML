# Project-Name-Myntra-Online-Retail-Customer-Segmentation-Unsupervised-ML

![image](https://github.com/user-attachments/assets/8ee5a16c-07d7-4535-afcc-f23ab1040933)

# Project Summary -
Myntra is a leading Indian fashion e-commerce company known for its wide range of clothing, accessories, and lifestyle products. While Myntra is recognized primarily for fashion, this dataset relates to the company's online retail operations for Myntra Gifts Ltd., a UK-based division specializing in unique all-occasion giftware. This dataset spans transactions from December 1, 2009, to December 9, 2011, and includes detailed records of sales made through Myntra Gifts Ltd.’s non-store online platform. The dataset provides a thorough snapshot of the company's international online retail activities during this period.

# Problem Statement
1. Which products are the most and least sold ones?

2. Which countries has the most and least number of customers?

3. Distribution of the numerical features.

4. Which day had the most and least number of purchases?

5. Which month had the most and least number of purchases?

6. Which hour in a day had the most and least number of purchases?

![image](https://github.com/user-attachments/assets/79016cfa-7ed8-4cd1-8c09-87818de0b482)

# Variables Description-

InvoiceNo: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction. If this code starts with letter 'c', it indicates a cancellation.

StockCode: Product (item) code. Nominal, a 5-digit integral number uniquely assigned to each distinct product.

Description: Product (item) name. Nominal.

Quantity: The quantities of each product (item) per transaction. Numeric.

InvoiceDate: Invoice Date and time. Numeric, the day and time when each transaction was generated.

UnitPrice: Unit price. Numeric, Product price per unit in sterling.

CustomerID: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer.

Country: Country name. Nominal, the name of the country where each customer resides.

![image](https://github.com/user-attachments/assets/46dc35bc-6abe-41ad-8b3a-e5e1fd70a1f3)

# Performing RFM Segmentation and RFM Analysis, step by step:

Step 1:
The first step in building an RFM model is to assign Recency, Frequency and Monetary values to each customer. The raw data for doing this, which should be readily available in the company’s CRM or transactional databases, can be compiled in an Excel spreadsheet or database.

Step 2:
The second step is to divide the customer list into tiered groups for each of the three dimensions (R, F and M), using Excel or another tool. Unless using specialized software, it’s recommended to divide the customers into four tiers for each dimension, such that each customer will be assigned to one tier in each dimension.

Step 3:
The third step is to select groups of customers to whom specific types of communications will be sent, based on the RFM segments in which they appear.

Step 4:
The fourth step actually goes beyond the RFM segmentation itself: crafting specific messaging that is tailored for each customer group. By focusing on the behavioral patterns of particular groups, RFM marketing allows marketers to communicate with customers in a much more effective manner.

# Apply log transformation to the RFM values and plot each distribution:

Applying a log transformation in the context of RFM (Recency, Frequency, Monetary) analysis, or any data analysis task, serves several important purposes:

Normalization: RFM metrics can vary significantly in scale. For example, monetary values can range from a few dollars to thousands, while frequency might vary from 1 to hundreds of times. A log transformation helps to normalize these scales, making it easier to compare and analyze data across different scales.

Handling Skewed Data: Many datasets, especially those involving monetary values or counts (like frequency), are often right-skewed, meaning most of the data points are clustered around the lower end of the scale with a long tail extending towards higher values. Log transformation helps in reducing the skewness, making the distribution more symmetrical and closer to a normal distribution. This is beneficial because many statistical methods and machine learning algorithms assume or perform better with data that is approximately normally distributed.

Reducing the Impact of Outliers: In RFM data, you might encounter extreme values or outliers, such as very high monetary values or unusually frequent purchases. These outliers can disproportionately influence the analysis. Log transformation reduces the impact of outliers by bringing them closer to the rest of the data points, thus providing a more balanced view.

![image](https://github.com/user-attachments/assets/1339c1b6-bf8e-4dbb-b391-544113d40542)

![image](https://github.com/user-attachments/assets/df69e3a8-17e9-4a6f-9aad-8f9c5d422b9d)

![image](https://github.com/user-attachments/assets/5b3b6afe-11f9-42ff-af72-16587cf54529)

# Conclusion-

# Cluster 1:

Recency: High (average around 165 days)
Frequency: Low (average around 15 transactions)
Monetary: Low (average around $286)
Interpretation: Customers in this cluster are likely to be 'At-Risk' or 'Lapsed' customers. They haven't made purchases recently, and when they did, they didn't do so very frequently and didn't spend much. These customers might have been one-time buyers or occasional shoppers. Engaging them with reactivation campaigns or exploring why they haven’t returned can be a strategic move.

# Cluster 0:

Recency: Very Low (average around 11 days)
Frequency: Very High (average around 259 transactions)
Monetary: Very High (average around $5933)
Interpretation: This cluster represents your 'Champions' or 'Loyal' customers. They shop frequently, recently, and spend the most. They are the most valuable segment, likely to respond positively to new offers, up-sell and cross-sell opportunities. Maintaining their high engagement level is crucial, and they can also be targeted for feedback or as brand ambassadors.

# Cluster 2:

Recency: Moderate (average around 68 days)
Frequency: Moderate (average around 69 transactions)
Monetary: Moderate (average around $1200)
Interpretation: Customers in this cluster can be seen as 'Potential Loyalists' or 'Promising' customers. They have a balanced score in all three RFM metrics. These customers have the potential to become more valuable if properly engaged. Tailored marketing strategies, loyalty programs, and incentives to increase their purchase frequency and value can be effective.

# Overall Strategy:

Cluster 1 ('At-Risk/Lapsed'): Focus on re-engagement strategies. Understand their needs and reasons for not returning. Offer incentives or feedback surveys to encourage them to revisit and make purchases.
Cluster 0 ('Champions/Loyal'): Prioritize maintaining their high level of engagement. Offer exclusive deals, loyalty programs, and early access to new products. They can also be engaged in referral programs.
Cluster 2 ('Potential Loyalists/Promising'): Encourage them to visit and buy more often. Personalized communication, recommending products based on past purchases, and loyalty rewards can be effective.
Thus, from our comparison table we can conclude that KMeans clustering on Recency, Frequency and Monetary data gives us the best result with the optimal number of clusters as 3. We can use this model to cluster our data in 3 segments and develop better marketing strategies.

## Hurrah! You have successfully completed your Machine Learning Capstone Project !!!




