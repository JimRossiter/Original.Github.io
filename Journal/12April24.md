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

The above code showed the number of international students corresponding to each stay. Once this was achieved, I ordered them in descending order. 
