# Amazon Vine Analysis 

## Overview of the analysis: Explain the purpose of this analysis.
In this project, we will be examining the paid reviews done by members of the Amazon Vine Program. "The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products." The data used is from Amazon's Review Datasets, and the selected dataset is on kitchen reviews.

Resources:
- PySpark, Google Colab
- Amazon AWS 
- PgAdmin, postgresSQL
- Amazon Review Datasets, 'kitchen' dataset 

In the first part of this analysis(Amazon_Reviews_ETL.ipynb), we will split the data into four tables: customers, products, reviews, and vine. Condensing the data into these groups will make it easier to understand and analyze. The tables will have the following data:
- Customers
  - customer id and customer count
- Products 
  - product id and product title
- Reviews (review_id)
  - review id, customer id, product id, product parent, and review date
- Vine (vine program reviews)
  - review id, star rating, helpful votes, total votes, vine, verified purchase 

After creating these tables using PySpark, we then connect our Amazon RDS and use it to import the table data into pgAdmin. 

## Results of Vine Analysis 
The second part of this analysis(Vine_Review_Analysis.ipynb), we will gather further information on the vine table. 

- The kitchen reviews dataset has 93,468 reviews in total. 
- The total number of paid reviews is 1,160. 
- The total number of unpaid reviews is 92,308.
- The total number of 5 star reviews is 43,736.

  - The total percentage of paid 5 star reviews out of all reviews is 0.52%.
  - The total percentage of unpaid 5 star reviews out of all reviews is 46.27%.

 - Out of all the paid reviews, 42.16% of them were 5 star reviews. 
- Out of all the unpaid reviews, 46.85% of them were 5 star reviews. 
- Out of all the reviews, 46.79% of them were 5 star reviews. 

  - Out of all 5 star reviews, 1.12% of them were paid.
  - Out of all 5 star reviews, 98.88% of them were unpaid.

## Summary: In your summary, state if there is any positivity bias for reviews in the Vine program. Use the results of your analysis to support your statement. Then, provide one additional analysis that you could do with the dataset to support your statement.
