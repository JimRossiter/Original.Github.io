## 14 April 2024 - Sub-queries and joining data in SQL

Today's dive into SQL was eye-opening, especially when it came to joining data. I spent some time with DataCamp's "Joining Data in SQL" course, and  I felt like I learnt a lot! I am starting to notice my skills are progressing and my understanding is growing.

I am attaching a query that I carried out that really appealed to me as it was more complex than what I was used to but I felt a great sense of accomplishment once I got my head around it. Here is the snippet:

```sql
-- Select fields from cities
SELECT 
	name, 
    country_code, 
    city_proper_pop, 
    metroarea_pop,
    city_proper_pop / metroarea_pop * 100 AS city_perc
FROM cities
-- Use subquery to filter city name
WHERE name IN
  (SELECT capital
   FROM countries
   WHERE (continent = 'Europe'
   OR continent LIKE '%America'))
-- Add filter condition such that metroarea_pop does not have null values
	  AND metroarea_pop IS NOT NULL
-- Sort and limit the result
ORDER BY city_perc DESC
LIMIT 10;
```

What's cool about this is how it brings together a few important ideas in SQL:

- **Subqueries**: It's like a mini-query inside the main one. In this code, the subquery finds capitals in Europe and the Americas, helping filter cities.

- **Inner Joins**: Even though we don't see it explicitly, the subquery is doing a kind of inner join between the `cities` and `countries` tables based on the country codes.

- **Filtering Techniques**: We add conditions to make sure we only get the data we need. Here, we're making sure `metroarea_pop` isn't null.

This experience showed me just how powerful SQL can be for slicing and dicing data. Looking forward to seeing what else I'll discover!

- Got introduced to subqueries, inner joins, and filtering in SQL.
- Saw how they work together to fetch specific data.
- Excited to keep exploring SQL and its capabilities.


