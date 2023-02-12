What issues will you address by cleaning the data?
- unit price does not make sence, needs to be divided by 1,000,000, as well as the product price

- In the sales report, the number of the ration has too many decimal places, needs to be clean by only 2 decimal places



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

- Cleaning data of "ratio" in table " sales report"
  * UPDATE sales_report
    SET ratio = ROUND(ratio*100, 2 );

