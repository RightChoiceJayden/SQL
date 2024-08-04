## Filtering SQL queries

<h2>Description</h2>

Investigating potential security issues and using SQL with filters to
perform security-related tasks.

<h2>Retrieve After Hours Failed Login Attempts</h2>

There were suspicious activities that occurred after business hours (after 18:00). All after hours
login attempts that failed need to be investigated.

I created a SQL query on MariaDB to filter for failed login attempts that occurred after business
hours.

![Screenshot 2024-08-03 at 8 11 20 PM](https://github.com/user-attachments/assets/17e91dcd-1cfe-4975-894b-a7df4d643c0e)

The result is based on the <mark>log_in_attempts</mark> table. The <mark>login_time</mark> column is after
18:00. The login attempts are failed (0). The filter “Select * “ means to select everything (all
columns) and FROM <mark>log_in_attempts</mark> means it is from the <mark>log_in_attempts</mark> table.
Success indicates the status of the login. If it is zero, it is a failure whereas if it is one, it is a
success. Therefore, there were 19 failed login attempts after 18:00.

<h2>Retrieve Login Attempts on Specific Dates</h2>

A suspicious event occurred on 2022-05-09. Any login activity that happened on 2022-05-09
and the day before needs to be investigated. I created a SQL query to filter for
login attempts that occurred on specific dates.

![Screenshot 2024-08-03 at 8 11 33 PM](https://github.com/user-attachments/assets/450045bb-7dc4-4fb1-b973-59125b60f9e3)
![Screenshot 2024-08-03 at 8 11 44 PM](https://github.com/user-attachments/assets/6e2ab5af-4548-49ea-83e7-3a56d7f03e4d)

I selected the <mark>log_in_attempts</mark> table and used the <mark>WHERE</mark> clause and <mark>OR</mark> operator to filter
the results to output only login attempts that occurred on 2022-05-09 or 2022-05-08. There were 75 login attempts in these two days.

<h2>Retrieve Login Attempts Outside of Mexico</h2>

After investigating the data, there is a strong indication that login
attempts outside of Mexico should be investigated.
I created a SQL query to filter for login attempts that occurred outside of Mexico.

![Screenshot 2024-08-03 at 8 11 56 PM](https://github.com/user-attachments/assets/8892a5f1-5b8c-471e-be03-f546ee1fe888)
![Screenshot 2024-08-03 at 8 12 07 PM](https://github.com/user-attachments/assets/f4333f57-42a2-4c7d-af8e-7293251c68c9)

Used the <mark>WHERE</mark> clause and <mark>NOT</mark> operator to filter the outputs and receive the login attempts
outside Mexico. However, the word “Mexico” could be “Mex”, “MEX”, and etc. To simplify this, I
chose <mark>LIKE</mark> with <mark>MEX%</mark> as the pattern to match as MEX and MEXICO. The % sign indicates any
unspecified characters when used with <mark>LIKE</mark>. There were 144 login attempts
outside Mexico.

<h2>Retrieve All Employees Not in IT</h2>

Created a SQL query to filter for employee machines from employees NOT in the Information
Technology department.

![Screenshot 2024-08-03 at 8 12 58 PM](https://github.com/user-attachments/assets/b7209009-72a0-4646-821d-63fa280ad24a)
![Screenshot 2024-08-03 at 8 13 11 PM](https://github.com/user-attachments/assets/db243f67-132b-4580-8207-a3e67846f4a9)

I selected all data from the employee table. Then, I used a <mark>WHERE</mark> clause with
<mark>NOT</mark> to filter for employees not in the IT department.

<h2>Summary</h2>
I applied filters to SQL queries to get specific information on employee and
log_in_attempts tables. I used the <mark>AND, OR, NOT</mark> operators to filter for the specific
information and I used <mark>LIKE</mark> and the <mark>(%)</mark> sign filter for patterns.

