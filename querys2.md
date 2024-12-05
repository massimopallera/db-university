> Querys


```SQL

-- 1)
SELECT count(id), year(enrolment_date)
FROM students
GROUP BY year(enrolment_date)
ORDER BY year(enrolment_date)  


--2) 


```