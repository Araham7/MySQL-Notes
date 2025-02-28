# Before executing the following code, ensure that the [lco_films](./lco_films) file is added to the database. You can do this using either VS-Code(using `SQLtools extension`) or `MySQL Workbench`.

### 1. `SELECT first_name, last_name, address, district FROM actor JOIN address ON actor.address_id = address.address_id  LIMIT 10;`
  - This query performs an `INNER JOIN` between the `actor` and `address` tables using the `address_id` column.and it will retrieves the first 10 rows of the `first_name`, `last_name`, `address`, and `district` columns of the `INNER JOIN`.

### 2. `SELECT first_name, last_name, address, district FROM actor LEFT OUTER JOIN address ON actor.address_id = address.address_id LIMIT 10;`
  - This query performs a `LEFT OUTER JOIN` between the `actor` and `address` tables using the `address_id` column.and It retrieves the first 10 rows, including all rows from the `actor` table and matching rows from the `address` table. If there is no match, `NULL` values are returned for the `address` table columns of the `LEFT OUTER JOIN`.

### 3. `SELECT first_name, last_name, address, district FROM actor RIGHT OUTER JOIN address ON actor.address_id = address.address_id LIMIT 10;` 
  - This query performs a `RIGHT OUTER JOIN` between the `actor` and `address` tables using the `address_id` column. and it retrieves the first 10 rows, including all rows from the `address` table and matching rows from the `actor` table. If there is no match, `NULL` values are returned for the `actor` table columns of the `RIGHT OUTER JOIN`.
