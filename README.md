#   ALTERING A TABLE

USE deff;

# ADDING A COLUMN TO AN EXISTING TABLE

SELECT *
FROM employees;

# ADDING THE SALARY COLUMN;
ALTER TABLE employees
ADD COLUMN salary DECIMAL(10,1);


# ADDING PHONE_NUMBER COLUMN AFTER THE GENDER COLUMN;
ALTER TABLE employees
ADD COLUMN phone_number CHAR(12)
AFTER gender;

# ADDING EMAIL ADDRESS COLUMN AFTER THE LAST_NAME COLUMN
ALTER TABLE employees
ADD COLUMN email VARCHAR(100)
AFTER last_name;


# UPDATING THE VARIOUS COLUMNS WITH THE REQUIRED DETAILS

# FOR THE EMAIL COLUMN
SELECT *
FROM employees;

UPDATE employees
SET email = 'uchenna@deff.com'
WHERE employee_id = 1;

UPDATE employees
SET email = 'gideon@deff.com'
WHERE employee_id = 2;

UPDATE employees
SET email = 'sarah@deff.com'
WHERE employee_id = 3;

UPDATE employees
SET email = 'onyiyechi@deff.com'
WHERE employee_id = 4;


# ADDING DETAILS TO THE PHONE_NUMBER AND SALARY COLUMNS TOGETHER,
SELECT *
FROM employees;

UPDATE employees
SET phone_number = '09134857464', salary = 32000
WHERE employee_id = 1;

UPDATE employees
SET phone_number = '08093739901', salary = 24000
WHERE employee_id = 2;

UPDATE employees
SET phone_number = '07092103277', salary = 29000
WHERE employee_id = 3;

UPDATE employees
SET phone_number = '09078900234', salary = 27000
WHERE employee_id = 4;

# DELETING A COLUMN FROM A TABLE AND ALSO A ROW FROM A TABLE;
# ADD A NEW EMPLOYEE;

INSERT INTO employees (first_name, last_name, email, gender, phone_number, salary)
VALUES	('Rita', 'Eze', 'rita@deff.com', 'female', '07090223465',21000);

SELECT *
FROM employees;

# TO DELETE THE NEWLY INSERTED ROW;
DELETE FROM employees
WHERE employee_id = 5;

# TO DELETE A COLUMN;
ALTER TABLE employees
DROP COLUMN phone_number;

SELECT *
FROM employees;

# TO DELETE THE WHOLE DETAILS FOUND IN THE TABLE;
TRUNCATE TABLE employees;
