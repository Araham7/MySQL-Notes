# 1. `mysql -u root -u` => To open the mysql server.(Then enter the `password`).

# 2. `show databases;` => To show the existing databases.

# 3. `CREATE DATABASE MOVIES_DB_PW;` => This will cretae a new Database.

# 4. `SHOW DATABASES;` => This will print all existing databases.

OUTPUT :---
```
+--------------------+
| Database           |
+--------------------+
| MOVIES_DB_PW       |
| PinkuDb            |
| information_schema |
| performance_schema |
| sys                |
+--------------------+
```

# 5. `use MOVIES_DB_PW;` => This will select the database `use MOVIES_DB_PW;`.

# 6. `CREATE TABLE Actors (Firstname VARCHAR(20), Lastname VARCHAR(20), Gender VARCHAR(10), Networth INTEGER);` => This will ctreate a table namely `Actors` (having columns `Firstname`, `Lastname` , `Gender` , `Networth`).

# 7. `DROP DATABASE PinkuDb;` => This will delete `PinkuDb`.

# 8. `SHOW TABLES`=> This will print all the tables preasent in the existing database.
OUTPUT:---
```
+------------------------+
| Tables_in_MOVIES_DB_PW |
+------------------------+
| Actors                 |
+------------------------+
```

# 9. `INSERT INTO Actors (Firstname, Lastname, Gender, Networth) VALUES ("Johnny", "Depp", "Male", 200);` => This will insert one actor into the `Actors` table.

# 10. `INSERT INTO Actors (Firstname, Lastname, Gender, Networth) VALUES ("Chris", "Hemsworth", "Male", 400);` => This will insert one actor into the `Actors` table.

# 11. `INSERT INTO Actors (Firstname, Lastname, Gender, Networth) VALUES ("Scarlett", "Johnson", "Female", 500), ("Chris", "Evans", "Male", 700), ("Paul", "Rudd", "Male", 150), ("Brie", "Larson", "Female", 650);` => This will add 4 rows at a time.

###  12. `SELECT * FROM Actors;` => This will print all of the rows of `Actors` table.(NOTE: Isme `*` ka matlab hai all-columns(saren columns)).
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Depp      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
+-----------+-----------+--------+----------+
```

# 13. `\! cls` or, `ctrl + C` => This will clear the entire screen of `windows` mysql terminal.

# 14. `clear` or, `ctrl + C` => This will clear the entire screen of `linux` and `MacOs` mysql terminal.

# 15. `SELECT * FROM Actors WHERE Networth >= 500;` => This will print the rows of the table whose `Networth` is greater then or equals to 500.(NOTE: Isme `*` ka matlab hai all-columns(saren columns)).
OUTPUT:---
```
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Chris     | Evans    | Male   |      700 |
| Brie      | Larson   | Female |      650 |
+-----------+----------+--------+----------+
```

# 16. `SELECT * FROM Actors WHERE Networth >= 500 OR Networth <= 200;` => This will print the rows of the table whose `Networth` is >= 500 OR <= 200.(NOTE: Isme `*` ka matlab hai all-columns(saren columns)).
OUTPUT:---
```
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Johnny    | Depp     | Male   |      200 |
| Scarlett  | Johnson  | Female |      500 |
| Chris     | Evans    | Male   |      700 |
| Paul      | Rudd     | Male   |      150 |
| Brie      | Larson   | Female |      650 |
+-----------+----------+--------+----------+
```

# 17. `SELECT Firstname, Networth FROM Actors WHERE Networth >= 500 OR Networth <= 200;` => This will print the `Firstname` and `Networth` of the Actors whose Networts >= 500 OR Networth <= 200.
OUTPUT:---
```
+-----------+----------+
| Firstname | Networth |
+-----------+----------+
| Johnny    |      200 |
| Scarlett  |      500 |
| Chris     |      700 |
| Paul      |      150 |
| Brie      |      650 |
+-----------+----------+
```

# 18. `SELECT * FROM Actors WHERE Gender = "Female";` => The will print the rows of all Female Genders.
OUTPUT:---
```
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Brie      | Larson   | Female |      650 |
+-----------+----------+--------+----------+
```

# 19. `SELECT Firstname, Networth FROM Actors WHERE Gender = "Female";` => This will print the rows of all femail genders of colums Firstname and Networth.
OUTPUT:---
```
+-----------+----------+
| Firstname | Networth |
+-----------+----------+
| Scarlett  |      500 |
| Brie      |      650 |
+-----------+----------+
```

# 20. `INSERT INTO Actors (Firstname, Lastname, Gender, Networth) VALUES ("Chadwick", "Boseman", "Male", 400);`

# 21. `SELECT * FROM Actors WHERE Firstname like '%a%';` => This will print all of the rows where Firstname starts with anything and ends with anything but `a` must be preasent in Firstname.

# 22. `INSERT INTO Actors (Firstname, Lastname, Gender, Networth) VALUES ("Araham", "Abeddin", "Male", 1000), ("Ahm", "Abddn", "female", 50), ("Huma", "Luni", "Male", 500);`


# 23. `SELECT * FROM Actors WHERE Firstname like 'ch%';` => This will print all of the rows which is having all of its Firstname starts with `ch`(Here ch is caseinsacitive).
OUTPUT:---
```
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Paul      | Rudd     | Male   |      150 |
| Chadwick  | Boseman  | Male   |      400 |
| Araham    | Abeddin  | Male   |     1000 |
| Ahm       | Abddn    | female |       50 |
| Huma      | Luni     | Male   |      500 |
+-----------+----------+--------+----------+
```

# 24. `SELECT * FROM Actors ORDER BY Networth ASC;` => 
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Ahm       | Abddn     | female |       50 |
| Paul      | Rudd      | Male   |      150 |
| Johnny    | Depp      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Chadwick  | Boseman   | Male   |      400 |
| Huma      | Luni      | Male   |      500 |
| Scarlett  | Johnson   | Female |      500 |
| Brie      | Larson    | Female |      650 |
| Chris     | Evans     | Male   |      700 |
| Araham    | Abeddin   | Male   |     1000 |
+-----------+-----------+--------+----------+
```

# 25. `SELECT * FROM Actors ORDER BY Networth DESC;` => 
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Araham    | Abeddin   | Male   |     1000 |
| Chris     | Evans     | Male   |      700 |
| Brie      | Larson    | Female |      650 |
| Huma      | Luni      | Male   |      500 |
| Scarlett  | Johnson   | Female |      500 |
| Chadwick  | Boseman   | Male   |      400 |
| Chris     | Hemsworth | Male   |      400 |
| Johnny    | Depp      | Male   |      200 |
| Paul      | Rudd      | Male   |      150 |
| Ahm       | Abddn     | female |       50 |
+-----------+-----------+--------+----------+
```

# 26. `SELECT * FROM Actors WHERE Firstname LIKE "ch%" ORDER BY Networth DESC;`
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Evans     | Male   |      700 |
| Chris     | Hemsworth | Male   |      400 |
| Chadwick  | Boseman   | Male   |      400 |
+-----------+-----------+--------+----------+
```

# 27. `SELECT * FROM Actors WHERE Firstname LIKE "ch%" ORDER BY Networth ASC;`
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |      400 |
| Chadwick  | Boseman   | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
```

# 28. `SELECT * FROM Actors ORDER BY Networth;` => This will print all rows bydefault assending order of `Networth`.
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Ahm       | Abddn     | female |       50 |
| Paul      | Rudd      | Male   |      150 |
| Johnny    | Depp      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Chadwick  | Boseman   | Male   |      400 |
| Huma      | Luni      | Male   |      500 |
| Scarlett  | Johnson   | Female |      500 |
| Brie      | Larson    | Female |      650 |
| Chris     | Evans     | Male   |      700 |
| Araham    | Abeddin   | Male   |     1000 |
+-----------+-----------+--------+----------+
```

# 29. `SELECT * FROM Actors WHERE Firstname LIKE "Ch%" ORDER BY Firstname ASC, Networth DESC;` => This will print the all rows of the `Actors` table whose `Firstname` starts with `Ch` and the will be printd in the Asending oder og Firstname as well as the are arrenged virtically desending order of `Networth`.
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chadwick  | Boseman   | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
| Chris     | Hemsworth | Male   |      400 |
+-----------+-----------+--------+----------+
```

# 30. `SELECT * from Actors LIMIT 3;` => This will print the only 5 rows of `Actors` table elements.
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Depp      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
+-----------+-----------+--------+----------+
```

# 31. `SELECT * FROM Actors LIMIT 3 OFFSET 0;` => This will print the first 3 rows of Actors table.(`OFFSET 0` without leaving any rows from top in `pagination`).
OUTPUT:---
```+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Depp      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
+-----------+-----------+--------+----------+
```

# 32. `SELECT * FROM Actors LIMIT 3 OFFSET 2;`=> This will print the 3 rows of Actors table.(`OFFSET 2` leaving 2 rows from top in `pagination`).
OUTPUT:---
```
+-----------+----------+--------+----------+
| Firstname | Lastname | Gender | Networth |
+-----------+----------+--------+----------+
| Scarlett  | Johnson  | Female |      500 |
| Chris     | Evans    | Male   |      700 |
| Paul      | Rudd     | Male   |      150 |
+-----------+----------+--------+----------+
```

# 33. `SELECT * FROM Actors WHERE Firstname LIKE "Ch%" LIMIT 2;` => This will print only first 2 rows whose firstname starts with `Ch`.
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Chris     | Hemsworth | Male   |      400 |
| Chris     | Evans     | Male   |      700 |
+-----------+-----------+--------+----------+
```

# 34. `UPDATE Actors SET Networth = 500000 WHERE Firstname = "Araham";` => This will update the `Networth` of the row whose `Firstname = Araham`.

# 35. `SELECT * FROM Actors;`
OUTPUT:---
```
+-----------+-----------+--------+----------+
| Firstname | Lastname  | Gender | Networth |
+-----------+-----------+--------+----------+
| Johnny    | Depp      | Male   |      200 |
| Chris     | Hemsworth | Male   |      400 |
| Scarlett  | Johnson   | Female |      500 |
| Chris     | Evans     | Male   |      700 |
| Paul      | Rudd      | Male   |      150 |
| Brie      | Larson    | Female |      650 |
| Chadwick  | Boseman   | Male   |      400 |
| Araham    | Abeddin   | Male   |   500000 |
| Ahm       | Abddn     | female |       50 |
| Huma      | Luni      | Male   |      500 |
+-----------+-----------+--------+----------+
```

# 36. `EXIT;` => This command will exit the user from the mySQL.
