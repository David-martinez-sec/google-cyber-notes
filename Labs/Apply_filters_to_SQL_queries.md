# Apply Filters to SQL Queries

## Project Description
In this project, I practiced applying SQL filters to investigate potential security incidents and gather employee information. The tasks focused on filtering for dates, times, countries, and departments. I used SQL clauses such as WHERE, AND, OR, NOT, and LIKE to refine results. These queries mirror real-world scenarios that security analysts face when working with authentication logs and employee databases.

---

## Step 3: Retrieve after hours failed login attempts

**Query:**
```sql
SELECT *
FROM log_in_attempts
WHERE login_time > '18:00'
  AND success = 0;
```

**Explanation:**
This query selects all records from the log_in_attempts table where the login_time occurred after 18:00 (6:00 PM) and the success value equals 0, meaning the login failed. Using AND ensures both conditions must be true for a row to be included. This helps identify potentially suspicious failed login attempts after business hours.

---

## Step 4: Retrieve login attempts on specific dates

**Query:**
```sql
SELECT *
FROM log_in_attempts
WHERE login_date = '2022-05-08'
   OR login_date = '2022-05-09';
```

**Explanation:**
This query retrieves all login attempts from the suspicious date (2022-05-09) and the day before (2022-05-08). The OR operator ensures that results are returned if either date condition is met. This lets me investigate activity around the event in question.

---

## Step 5: Retrieve login attempts outside of Mexico

**Query:**
```sql
SELECT *
FROM log_in_attempts
WHERE country NOT LIKE 'MEX%'
  AND country NOT LIKE 'MEXICO%';
```

**Explanation:**
This query pulls login attempts that did not originate from Mexico. The NOT LIKE operator excludes rows where the country column starts with "MEX" or equals "MEXICO". Using % as a wildcard ensures variations are caught, such as MEX or MEXICO.

---

## Step 6: Retrieve employees in Marketing

**Query:**
```sql
SELECT *
FROM employees
WHERE department LIKE '%Marketing%'
  AND office LIKE 'East%';
```

**Explanation:**
This query finds all employees in the Marketing department who are located in offices in the East building. The LIKE operator with % allows for partial matches, so it captures any office codes beginning with "East" (e.g., East-170, East-320).

---

## Step 7: Retrieve employees in Finance or Sales

**Query:**
```sql
SELECT *
FROM employees
WHERE department LIKE '%Finance%'
   OR department LIKE '%Sales%';
```

**Explanation:**
This query returns all employees who are in either the Finance or Sales departments. The OR operator ensures results are included if either condition is true.

---

## Step 8: Retrieve all employees not in IT

**Query:**
```sql
SELECT *
FROM employees
WHERE department NOT LIKE '%Information Technology%';
```

**Explanation:**
This query retrieves all employees who are not part of the Information Technology department. Using NOT LIKE excludes rows that contain 'Information Technology' in the department column, ensuring the update is applied to all other departments.

---

## Summary
This project demonstrated how to use SQL filters to investigate potential security issues and organize employee information. I used WHERE clauses with AND, OR, NOT, and LIKE to handle different filtering scenarios, such as time ranges, specific dates, country exclusions, and department-based queries. These skills are essential for security analysts when analyzing authentication logs or preparing targeted updates for employee systems.
