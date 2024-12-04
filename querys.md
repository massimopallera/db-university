> query

1) SELECT * FROM students WHERE date_of_birth >= "1990-01-01" AND date_of_birth <= "1990-12-31"
2) SELECT * FROM courses WHERE cfu > 10

 <!--curdate gets the current date  -->
3) SELECT * FROM students WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) = 30;

4) SELECT * FROM courses WHERE year=1 AND period="I semestre"

5)  SELECT * FROM exams WHERE date = "2020/06/20" AND HOUR(hour) >= 14

6)  SELECT * FROM degrees WHERE level="magistrale"

7)  SELECT count(id) as Departments FROM departments
8)  SELECT * FROM teachers WHERE phone is null

<!-- with null at the first column, I'll bypass the primary key -->
9) INSERT students
VALUES (NULL, 34, "Massimo", "Pallera", "2004/04/23","PLLMSM", "2024/04/15", "31341544", "pallera.massimo@gmail.com")

10) UPDATE teachers
SET phone="126"
WHERE name="Pietro" AND surname ="Rizzo"

11) DELETE FROM students WHERE email="pallera.massimo@gmail.com"