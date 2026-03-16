# Apply filters to SQL queries

## Project description
In this project, my task is to examine the organization’s data in their employees and log_in_attempts tables. I will use SQL filters to retrieve records from different datasets and investigate the potential security issues.

## Retrieve after hours failed login attempts
`Select * 
FROM log_in_attempts
WHERE login_time > ‘18:00’ AND success = 0;`

This query selects all data from the log_in_attempts table on the dates 2022-05-09 or 2022-05-08. 

## Retrieve login attempts outside of Mexico
`SELECT *
FROM log_in_attempts
WHERE NOT country LIKE ‘Mex%’;`

This query selects all data from the log_in_attempts table where login attempts were not in Mexico. I used `NOT` country to show data outside of Mexico, and I used country `LIKE ‘Mex%’` to filter
the countries that start with ‘Mex’. `LIKE` searches for patterns, and `%` represents any characters

## Retrieve employees in Marketing
`SELECT * 
FROM employees 
WHERE department = 'Marketing' AND office LIKE 'East%';`

This query selects all data from employees table and filters to show the ones in the Marketing department and located in the East building. I used `LIKE East%` to 
filter to any employee in the East building. I used AND to filter employees that have both of these requirements.

## Retrieve employees in Finance or Sales
`SELECT * 
FROM employees 
WHERE department = 'Finance' OR department = 'Sales';`

This query selects all data from employees table and filters to show employees in the finance or sales department. I used `OR` to show employees with either Finance and/or Sales.

## Retrieve all employees not in IT
`SELECT * 
FROM employees 
WHERE NOT department = 'Information Technology';`

This query selects all data from the employees table and filters to show employees who are not in the IT department. I used `NOT` to show everyone who is not listed as IT.

## Summary
I did all the previous tasks using different SQL filters like AND, OR, NOT, and LIKE. Using these filters allowed me to find important information faster. I was 
able to find out failed login attempts, login attempts on days that had suspicious events, login attempts outside of Mexico, and finding employees in specific departments and buildings. 
SQL filters helped me retrieve all this information and investigate potential security issues.


