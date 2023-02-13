What are your risk areas? Identify and describe them.

- All the database, especially the table of "all sessions", so many columns with the title are ambiguous. When we analysis a table, we need to understand what each of them were talking about and then we can clean and filter the data. What we did in QA process, is to make sure there is no missing data, as well as the accuracy of the data for each analysist.

- Besides, we need to know and difine what expectation we would like to get. Look each table and each columns, to make sure every single column has it's own meaning. Otherwise, we need to transfer them into a meaning value. 
Like the unit price and product price. 


QA Process:
Describe your QA process and include the SQL queries used to execute it.

QA process:

- Check the missing data in SQL: (for examples)

  * SELECT *

    FROM products

    WHERE "name" IS NULL

  * SELECT * 

    FROM analytics

    WHERE "visitId" is null OR "fullvisitorId" is null

  * SELECT *  

    FROM all_sessions

    WHERE "productPrice" IS NULL

- Check the data accuracy in SQL (for example: we can check the product SKU with the product name are the same in each tables, like "product" table and "sales_report" table):
  
  * SELECT p."SKU", p."name", s."name" AS "others"

    FROM products p

    JOIN sales_report s ON p."SKU" = s."productSKU"

    WHERE p."name" != s."name" ; 

All the checking results are null, which means there is no error for those columns.


