What are your risk areas? Identify and describe them.



QA Process:
Describe your QA process and include the SQL queries used to execute it.

- Check duplicate values in "all sessions" table 
SELECT "visitId", COUNT(*) AS B
FROM all_sessions
GROUP BY "visitId"
HAVING COUNT (*) > 1;