# Customer Segmentation for Bookstore E-Commerce using RFM Analysis (Binning and K-Means Method)
## 1.	Introduction
### A.	Business Undestanding

Company Book & Gift, second largers bookstore company in Europe, that sells various books from any genre has decline sales approximately 10% for 2 month. After make an analysis, Market Team conclude that the marketing initiative that has been created from the company doesnt targeted fit into the right segment. For make a better marketing initiative, Marketing Team should define dan create a robust segmented customer layer to create initiative of marketing campaign. Another issue is the resource that want to be allocated is limited, so it should be spread efficiently. Company Book & Gift must recognizes customers behavior that have the same needs, preferences, or purchasing behaviors.

The Book & Gift is a well-established retail business specializing in selling books, e-books, and related products. With the rapid evolution of the retail industry and changing consumer preferences, the company recognizes the need to better understand its customer base and tailor its marketing strategies accordingly. To achieve this goal, the company has decided to embark on a customer segmentation project.

The customer segmentation project will involve analyzing historical customer data, transaction records, and customer interactions to identify distinct customer segments. These segments will be used to refine marketing strategies, enhance customer engagement, and ultimately drive business growth. By undertaking this customer segmentation project, the Bookstore Company aims to enhance its customer relationships, increase sales, and optimize its marketing efforts. With a deeper understanding of its customer base, the company can adapt to changing market dynamics and provide a more personalized shopping experience, ultimately securing its position in the competitive retail landscape.

The input of this problem is ineffective marketing targeting. So we will to use Binning & K-Means method to create market segmentation. Hopefully, those market segment can be implement specific marketing strategies to increase sales.

### B.	Business Objective

- Increase Sales
  
Increase overall sales by targeting specific customer segments with tailored marketing strategies and product recommendations.

-	Improve Customer Experience
  
Enhance the shopping experience by offering personalized recommendations and promotions.

-	Optimize Inventory
  
Improve inventory management by stocking products that align with the preferences of different customer segments.

-	Reduce Marketing Costs
  
Reduce marketing expenses by focusing resources on high-potential customer segments.

### C.	Deliverables:

- Customer Segmentation Report: Detailed analysis of customer segments, including profiles and recommendations.
- Implementation Plan: A roadmap for executing the segmented marketing strategies.
- Training: Training sessions for relevant teams on how to use customer segments effectively.

## 2.	Related Works

- The Customer Base Audit – Peter Fader
- Customer Analytics for Dummies – Wiley (2015) by Jeff Sauro
- Modeling Markets – by Peter S.H Leeflang, Jaap E. Wieringa, Tammo H.A. Bijmolt, Koen H. Pauwels
- Market Segmentation Analysis (2018) – by Sara Dolnicar, Bettina Grun, Friedrich Leisch
- Database Marketing (2008) – by Robert C. Blattberg, Byung-Do Kim, Scott A. Neslin
- Research on K-Value Selection Method of K-Means Clustering Algorithm (2019) – by Yuan, C. & Yang, H
- Lecture Notes 11 Clustering – Carnegie Mellon University – by Amit K Verma, Anthony (Tony) Rollet
- Lecture Notes Clustering – Universitat Heidelberg by Erich Schubert
- Visualizing RFM Segmetation by Ron Kohavi and Rajesh Parekh

## 3.	Dataset & Features

For create the analysis, we use the dataset with features as follows
- Customer ID	: Customer number. Nominal, a 5-digit integral number uniquely assigned to each customer. 
-	Invoice		: Invoice number. Nominal, a 6-digit integral number uniquely assigned to each transaction.
-	Revenue_Total	: Total revenue that generated from unique customer from first buy.
-	N_Purchases	: The quantities of each product (item) per transaction. Numeric.
-	Purchase_DATE	: Purchase Date and time. Numeric, the day when each transaction was generated. 
-	Purchase_VALUE: Unit price. Numeric, Product price per unit in sterling.
-	Pay_Method	: Method for purchase the item (Cards, PayPal, Digital Wallets).
-	Time_Spent	: Average time of customer on website (in second).
-	Browser	: Chrome, Safari, Edge, Other.
-	Newsletter	: Subscribed or Not Subscribed 
-	Voucher	: Used or Not Used 
Source of original dataset can be access through this link:
https://www.kaggle.com/datasets/onlineretailshop/online-shop-customer-sales-data

Because we will do unsupervised learning at this project, we wouldn’t split dataset into training, validation, and testing. From the dataset, we need to typecasting the Purchase_DATE into datetime format. Also, we will normalize the data if there is very skew feature after being analyst. Normalization will be apply by using log term to make distribution spread normally. Here the example of dataset:
![image](https://github.com/axeltanjung/rfm_segmentation/assets/87402782/1b68e797-84ed-406f-be66-1d2175b14d52)

