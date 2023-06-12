## Experiment 4
## Aim:
To create SQL query to show record from one table that another table does not have.

## Algorithm:
1.Start MYSQL Workbench.

2.Create a database to store your data.

3.Use the database and create a table.

4.Inside the table ,create variables with appropriate datatype.

5.Insert values and apply logic to visualize the output.

## Program:
```
CREATE TABLE Employee (
	WORKER_ID INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
	FIRST_NAME CHAR(25),
	LAST_NAME CHAR(25),
	EmployeeSalary INT(15),
	JOINING_DATE DATETIME,
	DEPARTMENT CHAR(25)
);
CREATE TABLE Manager (
	WORKER_ID INT NOT NULL PRIMARY KEY AUTO_INCREMENT,
	FIRST_NAME CHAR(25),
	LAST_NAME CHAR(25),
	ManagerSalary INT(15),
	JOINING_DATE DATETIME,
	DEPARTMENT CHAR(25)
);
SELECT * FROM EmployeeSalary
MINUS
SELECT * FROM ManagerSalary;
SELECT EmployeeSalary.*
FROM EmployeeSalary
LEFT JOIN
ManagerSalary USING (EmpId)
WHERE ManagerSalary.EmpId IS NULL;
```
## Result:
Therefore we have successfully created a SQL query to show record from one table that another table does not have.
