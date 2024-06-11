# Apply filters to SQL queries

## Objective

In this scenario, you need to obtain specific information about employees, their machines, and the departments they belong to from the database.
Your team needs data to investigate potential security issues and to update computers.
You are responsible for filtering the required information from the database.

### Skills Learned

- Run SQL queries to retrieve information from a database
- Advanced understanding of how to apply AND, OR, and NOT operators to filter SQL queries

### Tools Used

- MariaDB Shell.

## Senario 1 - Retrieve after hours failed login attempts

You recently discovered a potential security incident that occurred after business hours. To investigate this, you need to query the 'log_in_attempts' table and review after hours login activity. Use filters in SQL to create a query that identifies all failed login attempts that occurred after 18:00.

To acheive the above objective we need to use the 'SELECT *' so we can view all columns.
Now we need the 'FROM' as in which table do we need the data from, In this case we need to use the 'log_in_attempts' table which gives us access to the data we need.
We use the 'WHERE' operator to filter out the specific data we want to see. In this case we need the data from the 'login_time' & 'success' column, we dont need to use single quotes around the 'success' value as they are not string data. They are Boolean data

![image](https://github.com/Matt4llan/SQL/assets/156334555/97bda5fb-bd7a-4ba4-be26-44e9529bcd4a)

## Senario 2 - Retrieve login attempts on specific dates

A suspicious event occurred on 2022-05-09. To investigate this event, you want to review all login attempts which occurred on this day and the day before. Use filters in SQL to create a query that identifies all login attempts that occurred on 2022-05-09 or 2022-05-08.

To acheive the above objective we need to use the 'SELECT *' so we can view all columns.
Now we need the 'FROM' as in which table do we need the data from, In this case we need to use the 'log_in_attempts' table which gives us access to the data we need.
We use the 'WHERE' operator to filter out the specific data we want to see. In this case we need data from the 'login_date' column, as there are 2 dates to search between we can use the 'OR' operator

![image](https://github.com/Matt4llan/SQL/assets/156334555/347c9915-c24c-400a-a6ea-1a6640af7efa)

## Senario 3 - Retrieve login attempts outside of Mexico

There’s been suspicious activity with login attempts, but the team has determined that this activity didn't originate in Mexico. Now, you need to investigate login attempts that occurred outside of Mexico. Use filters in SQL to create a query that identifies all login attempts that occurred outside of Mexico.

To acheive the above objective we need to use the 'SELECT *' so we can view all columns.
Now we need the 'FROM' as in which table do we need the data from, In this case we need to use the 'log_in_attempts' table which gives us access to the data we need.
We use the 'WHERE' & 'NOT' operator to filter out countires NOT in Mexico. In this case we need the data from the 'country' column, as there are 2 different data enties for Mexico 'MEXICO' & 'MEX' we need to use a wildcard 'MEX%'

![image](https://github.com/Matt4llan/SQL/assets/156334555/db872eaf-2e96-4bbb-ae75-93773f374620)

## Senario 4 - Retrieve employees in Marketing

Your team wants to perform security updates on specific employee machines in the Marketing department. You’re responsible for getting information on these employee machines and will need to query the employees table. Use filters in SQL to create a query that identifies all employees in the Marketing department for all offices in the East building.

To acheive the above objective we need to use the 'SELECT *' so we can view all columns.
Now we need the 'FROM' as in which table do we need the data from, In this case we need to use the 'employees' table which gives us access to the data we need.
We use the 'WHERE' & 'AND' operator to filter out the specific data we want to see. In this case we need the data from the 'Department' & 'Office' column, as there are different data enties for the East Office we need to use a like wildcard 'EAST%' This query returns all records with values in the Office column that start with the pattern of 'EAST'. This means all offices e.g 'EAST-170' and 'EAST-195' are returned.

![image](https://github.com/Matt4llan/SQL/assets/156334555/5aca8972-df2e-43a1-ba8b-bca10eb3f61c)

## Senario 5 - Retrieve employees in Finance or Sales

Your team now needs to perform a different security update on machines for employees in the Sales and Finance departments. Use filters in SQL to create a query that identifies all employees in the Sales or Finance departments

To acheive the above objective we need to use the 'SELECT *' so we can view all columns.
Now we need the 'FROM' as in which table do we need the data from, In this case we need to use the 'employees' table which gives us access to the data we need.
We use the 'WHERE' & 'OR' operator to filter out the specific data we want to see. In this case we need the data from the 'Department' column.

![image](https://github.com/Matt4llan/SQL/assets/156334555/a003f938-f0d3-459a-bdc0-59d8acbc97b3)

## Senario 6 - Retrieve all employees not in IT

Your team needs to make one more update to employee machines. The employees who are in the Information Technology department already had this update, but employees in all other departments need it. Use filters in SQL to create a query which identifies all employees not in the IT department.

To acheive the above objective we need to use the 'SELECT *' so we can view all columns.
Now we need the 'FROM' as in which table do we need the data from, In this case we need to use the 'employees' table which gives us access to the data we need.
We use the 'WHERE' & 'NOT' operator to filter out Employees NOT in the Information Technology department. In this case we need the data from the 'Department' column.

![image](https://github.com/Matt4llan/SQL/assets/156334555/fe4330e5-bdde-4bbf-9106-086a729fd78d)




