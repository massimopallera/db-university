> query

1) SELECT * FROM students WHERE date_of_birth >= "1990-01-01" AND date_of_birth <= "1990-12-31"
2) SELECT * FROM courses WHERE cfu > 10

 <!--curdate gets the current date  -->
3) SELECT * FROM students WHERE TIMESTAMPDIFF(YEAR, date_of_birth, CURDATE()) = 30;