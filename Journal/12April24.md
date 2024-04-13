*12 April 2024*
## Analysing Students Mental Health Project 

For this inquiry, I was tasked with analysing the mental health of students who were studying away from home. The main focus of the investigation was the international students. Each student answered 3 surveys which investigated their depression scores, social connection scores and stress levels. 

```sql
SELECT
	stay,
	COUNT(*) as count_int,
	ROUND(AVG(todep),2) as average_phq,
	ROUND(AVG(tosc),2) as average_scs,
	ROUND(AVG(toas),2) as average_as
FROM students
WHERE Inter_dom='Inter' --only counting International students--
GROUP BY stay
ORDER BY stay DESC;
```

The above code returned the number of international students corresponding to each stay. Once this was achieved, I ordered them in descending order. I concluded that the length of stay correlated with high scores of depression and low scores of social connection. This is somewhat expected as feelings of homesickness and loneliness may creep in the longer that international students spend away from home. 

```sql

SELECT
	"Region"
	COUNT(Inter_dom) AS count_inter_dom
FROM students
WHERE Inter_dom='Inter'
GROUP BY "Region";

```

Next, I grouped together International students by the region they were from. This was interesting to investigate the relationship between their home region and their survey scores.

