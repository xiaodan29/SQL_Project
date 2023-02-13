What issues will you address by cleaning the data?
- unit price does not make sence, needs to be divided by 1,000,000, as well as the product price

- Cleaning date of "Total transaction Revenue" in "all sessions" table, it still does not make sense with the huge number.

- In the sales report, the number of the ration has too many decimal places, needs to be clean by only 2 decimal places.

- In the all session table, there are too many colunms, which need to be checked one by one. The city names are associated with the wrong country names which need to be corrected.




Queries:
Below, provide the SQL queries you used to clean your data.
- Cleaning data of "unit price" and "product price" :
  * UPDATE analytics
    SET unit_price =unit_price / 1000000;
  * UPDATE analytics
    SET unit_price = ROUND(unit_price, 2);

  * UPDATE all_sessions
    SET productPrice =productPrice / 1000000;
  * UPDATE all_sessions
    SET "productPrice" = ROUND ("productPrice", 2);

- Cleaning date of "Total transaction Revenue" in "all sessions" table
  * UPDATE all_sessions
    SET "totalTransactionRevenue" = ROUND("totalTransactionRevenue"/1000000, 2);     


- Cleaning data of "ratio" in table " sales report"
  * UPDATE sales_report
    SET ratio = ROUND(ratio*100, 2 );

- Correcting city and country names in "all session" table
  Here is the one example I did the change:
  * UPDATE all_sessions

    SET country = 'Ireland'

    WHERE country = 'Netherlands' AND city = 'Dublin'
  There are like 20 mistakes in those city and country names, so I did it one by one.
