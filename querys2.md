> Querys


```SQL

-- 1)
SELECT count(id) AS "Number of students", year(enrolment_date) AS "Year of enrollment"
FROM students
GROUP BY year(enrolment_date)
ORDER BY year(enrolment_date)  


-- 2) 
SELECT count(id) AS "Number of teachers", office_address AS "Office Address"
FROM teachers
GROUP BY office_address

-- 3)
SELECT avg(vote)
FROM exam_student
GROUP BY exam_id

-- 4)
SELECT count(degrees.id) AS "Courses number", d.name AS "Departments name"
FROM degrees
JOIN departments AS d ON degrees.department_id = d.id
GROUP BY department_id

```