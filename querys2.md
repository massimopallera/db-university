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

-- JOINS
-- 1) 
SELECT s.id, s.name, s.surname
FROM students AS s
JOIN degrees AS d ON d.id = s.degree_id
WHERE d.name = "Corso di Laurea in Economia"

-- 2)
SELECT dg.name
FROM degrees AS dg
JOIN departments AS d ON dg.department_id = d.id
WHERE d.name = "Dipartimento di Neuroscienze" 
AND dg.level = "magistrale"


-- 3)
SELECT c.*
FROM course_teacher AS ct
JOIN teachers AS t ON t.id = ct.teacher_id
JOIN courses AS c ON c.id = ct.course_id
WHERE t.id = 44 -- Fulvio Amato

-- 4)
SELECT s.name, s.surname, d.name, dp.name
FROM students AS s
JOIN degrees AS d ON d.id = s.degree_id
JOIN departments AS dp ON dp.id = d.department_id
ORDER BY s.name, s.surname

-- 5) 
SELECT c.name AS "Courses", t.name AS "Teacher Name", t.surname AS "Teacher Surname"
FROM course_teacher AS ct
JOIN teachers AS t ON ct.teacher_id = t.id
JOIN courses AS c ON ct.course_id = c.id
JOIN degrees AS d ON c.degree_id = d.id

-- 6)


```