*April 11th 2024*
## SQL Fundamentals
---
This week has been enjoyable on my journey into the world of SQL on DataCamp. Here are some key points I've learned, with some examples of key learnings:

1. **Understanding SQL Basics**: Mastering common SQL keywords such as SELECT, FROM, WHERE, AND, OR, and BETWEEN was crucial. For instance, using WHERE to filter data based on conditions like age > 30 or name = 'John' helped me extract specific subsets of data from tables.

2. **Exploring Joins**: Looking into different types of joins like INNER JOIN, LEFT JOIN, RIGHT JOIN, and FULL JOIN was challenging at first. I watched a good YouTube video from Alex the Analyst and now have a better grasp. For example, when combining data from two tables based on a common column (e.g., employee ID), INNER JOIN returns only matching rows, while LEFT JOIN returns all rows from the left table and matching rows from the right table.

3. **Mastering Join Queries**: Constructing join queries efficiently using ON clauses was essential. For instance, joining tables on multiple columns like ON A.ID = B.ID AND A.Name = B.Name helped me merge datasets accurately, considering multiple criteria. I find the picture below a help also.

   ![](/images/sqljoins.png)

4. **Using UNION and UNION ALL**: Understanding the difference between UNION and UNION ALL. When combining the results of two SELECT statements, UNION removes duplicates, while UNION ALL retains all rows, even duplicates.

5. **Code Writing Convention**: Adhering to code the writing convention set out by Holywell, such as using uppercase for SQL keywords and lowercase for table and column names, improves code readability. For example, writing SELECT column1, column2 FROM table_name instead of select Column1, Column2 from TableName enhances clarity. It is better for collaboration to have standard practice.

6. **Applying Aliases**: Utilizing aliases for tables and columns improved query clarity. For example, using aliases like SELECT e.ID AS EmployeeID, e.Name AS EmployeeName FROM Employees e reduced typing and made queries more concise.

7. **Handling NULL Values**: Understanding how to handle NULL values using IS NULL and IS NOT NULL functions was essential. For instance, using IS NULL to find records with missing values in a certain column like WHERE age IS NULL helped identify incomplete data. 

8. **Optimizing Query Performance**: Employing techniques like using indexes and minimizing wildcard characters in WHERE clauses enhanced query performance. For example, adding indexes to frequently queried columns like employee ID improved query execution speed.

9. **Data Filtering Techniques**: Practiced various data filtering techniques, such as using IN and NOT IN operators, improved my skills. For instance, using WHERE department IN ('HR', 'Finance') filtered records based on specific department names.

10. **Practice and Application**: Regularly practicing coding exercises and real-world scenarios on DataCamp's platform reinforced my understanding of SQL. For example, solving exercises that involved joining multiple tables and filtering data sharpened my SQL skills and problem-solving abilities.

Overall, this week's journey has equipped me with valuable SQL skills and insights that I'm eager to apply in future data analysis projects. 

---
**Common queries to remember:**
```sql
SELECT *
FROM population

LIMIT 5;

ORDER BY founding_year DESC
ORDER BY person_age ASC
```


