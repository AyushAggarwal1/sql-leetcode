- **Leetcode Problem No.** - 1378

- **Leetcode Link** - https://leetcode.com/problems/replace-employee-id-with-the-unique-identifier/description
- **Problem statement** - Replace Employee ID With The Unique Identifier
```
Table: Employees

+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| id            | int     |
| name          | varchar |
+---------------+---------+
```
id is the primary key (column with unique values) for this table.
Each row of this table contains the id and the name of an employee in a company.
 
```
Table: EmployeeUNI

+---------------+---------+
| Column Name   | Type    |
+---------------+---------+
| id            | int     |
| unique_id     | int     |
+---------------+---------+
```
(id, unique_id) is the primary key (combination of columns with unique values) for this table.
Each row of this table contains the id and the corresponding unique id of an employee in the company.
 

Write a solution to show the unique ID of each user, If a user does not have a unique ID replace just show null.

Return the result table in any order.

**Solution** -
```
# Write your MySQL query statement below
select unique_id ,name
from employees as emp
left join employeeUNI as uni
on uni.id = emp.id
```