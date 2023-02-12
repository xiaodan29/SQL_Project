Question 1: 
 - What kind of product had ordered the most (what is the most popular product name? )

SQL Queries:

SELECT "productSKU", "name", MAX("total_ordered")AS "most_popular"

FROM sales_report

GROUP BY "productSKU","name", "total_ordered"

LIMIT 1

Answer: 

PRODUCT SKU :   "GGOEGOAQ012899"    
 NAME       :    "Ballpoint LED Light Pen"       
 MOST POPULAR:  456

![](qq1.png)

Question 2: 
- How many transactions were made by visitors from each country? 

SQL Queries:

Answer:



Question 3: 
- what is the restock level for each product? 

SQL Queries:

Answer:


