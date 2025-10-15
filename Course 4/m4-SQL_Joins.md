# Comparing Types of Joins in SQL

When working in SQL, joins are used to combine data from multiple tables that share a common column. Different types of joins return different sets of rows.

---

## Inner Joins

**Definition:**  
- `INNER JOIN` returns rows that match on a specified column that exists in both tables.  
- Only matching rows are included in the results.  
- All specified columns are returned from both tables.

**Example (all columns):**
```sql
SELECT *
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```

**Example (specific columns):**
```sql
SELECT username, operating_system, employees.device_id
FROM employees
INNER JOIN machines ON employees.device_id = machines.device_id;
```
- If a column exists in both tables (e.g., `device_id`), you must specify the table name with the column (`employees.device_id`).

---

## Outer Joins

Outer joins expand results by including unmatched rows from one or both tables.  

### Left Joins

**Definition:**  
- `LEFT JOIN` returns all records from the left (first) table and only the matching rows from the right (second) table.  

**Syntax:**
```sql
SELECT *
FROM employees
LEFT JOIN machines ON employees.device_id = machines.device_id;
```
- All rows from `employees` are returned.  
- Only rows with a matching `device_id` are returned from `machines`.

---

### Right Joins

**Definition:**  
- `RIGHT JOIN` returns all records from the right (second) table and only the matching rows from the left (first) table.  

**Syntax:**
```sql
SELECT *
FROM employees
RIGHT JOIN machines ON employees.device_id = machines.device_id;
```
- All rows from `machines` are returned.  
- Only rows with a matching `device_id` are returned from `employees`.

**Note:**  
- Switching the order of the tables in a `LEFT JOIN` can give the same results as a `RIGHT JOIN`.  

Example (equivalent queries):
```sql
-- LEFT JOIN
SELECT *
FROM employees
LEFT JOIN machines ON employees.device_id = machines.device_id;

-- Equivalent RIGHT JOIN
SELECT *
FROM machines
RIGHT JOIN employees ON employees.device_id = machines.device_id;
```

---

### Full Outer Joins

**Definition:**  
- `FULL OUTER JOIN` returns all records from both tables.  
- Think of it as merging two tables completely.  
- Matching rows are aligned; unmatched rows from both tables are also included.  

**Syntax:**
```sql
SELECT *
FROM employees
FULL OUTER JOIN machines ON employees.device_id = machines.device_id;
```
- The order of tables does not affect the results.

---

## Key Takeaways

- **INNER JOIN**: returns only rows where both tables match.  
- **LEFT JOIN**: returns all rows from the left table and matches from the right.  
- **RIGHT JOIN**: returns all rows from the right table and matches from the left.  
- **FULL OUTER JOIN**: returns all rows from both tables.  

Joins are essential for combining and analyzing related data across multiple tables in a database.
