## April 15th - CASE WHEN queries

Today, I learned about using CASE WHEN in SQL to make decisions in a query. It's like using if-else statements that I am familiar with in Excel. This skill will be handy whenever I need to categorize or transform data based on specific conditions in SQL queries.

Here's a simple example to illustrate:

Let's say we have a table called `students` with columns `student_id`, `first_name`, `last_name`, and `grade`.

```sql
SELECT 
    first_name,
    last_name,
    grade,
    CASE 
        WHEN grade >= 90 THEN 'A'
        WHEN grade >= 80 THEN 'B'
        WHEN grade >= 70 THEN 'C'
        ELSE 'F'
    END AS letter_grade
FROM 
    students;
```

In this example, we're selecting the first name, last name, and grade of each student from the `students` table. The CASE WHEN statement checks the value of the `grade` column for each student. If the grade is 90 or above, it assigns the letter 'A', if it's between 80 and 89, it assigns 'B', and so on. If none of the conditions are met, it assigns 'F'. This helps in converting numerical grades into letter grades for easier understanding. Very helpful in my teaching career!

Other queries that interested me are found below:
```sql

SELECT 
	CASE WHEN hometeam_id = 10189 THEN 'FC Schalke 04'
        WHEN hometeam_id = 9823 THEN 'FC Bayern Munich'
         ELSE 'Other' END AS home_team,
	COUNT(id) AS total_matches
FROM matches_germany
GROUP BY home_team;
```
🔼 This query looked at the matches in the German football league between FC Schalke 04 and Bayern Munich. The output was a table which counted the number of games outside of this fixture, classified as 'Other' and the result for Schalke 04 and Bayern Munich was 68. This meant they played each other on 68 occasions.

---

```sql
SELECT 
	m.date,
	t.team_long_name AS opponent,
	Case WHEN m.home_goal > m.away_goal THEN 'Barcelona win!'
        WHEN m.home_goal < m.away_goal THEN 'Barcelona loss :(' 
        ELSE 'Tie' END AS outcome 
FROM matches_spain AS m
LEFT JOIN teams_spain AS t 
ON m.awayteam_id = t.team_api_id
WHERE m.hometeam_id = '8634' ;
```
🔼 I liked this query as it made sense of a large data set and we could gather insights very succinctly from the resulting output. It analysed the results of Barcelona FC's home games from the given season. Good practice of left join: all the matches in the Spanish league were matched up with the involved away teams using the ON keyword. The team's long name was selected but the syntax made this slightly more confusing. Barcelona'S team ID was 8634.

