Answer the following questions and provide the SQL queries used to find the answer.

    
**Question 1: Which cities and countries have the highest level of transaction revenues on the site?**


SQL Queries:

SELECT "city", "country", SUM("totalTransactionRevenue") as "total_Revenue"
FROM all_sessions
WHERE "totalTransactionRevenue" IS NOT null
GROUP BY "city", "country"
ORDER BY "total_Revenue" DESC;


Answer:
CITY                        COUNTRY              TOTAL REVENUE
not availableindemo dataset	United States	    6092.56
San Francisco	          United States	        1564.32
Sunnyvale	              United States     	992.23



**Question 2: What is the average number of products ordered from visitors in each city and country?**


SQL Queries:



Answer:





**Question 3: Is there any pattern in the types (product categories) of products ordered from visitors in each city and country?**


SQL Queries:



Answer:





**Question 4: What is the top-selling product from each city/country? Can we find any pattern worthy of noting in the products sold?**


SQL Queries:



Answer:





**Question 5: Can we summarize the impact of revenue generated from each city/country?**

SQL Queries:



Answer:







