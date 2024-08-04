## SQL JOIN

<h2>Description</h2>

Applied SQL join to play with the values
of the two tables. This task is related to relational database management.

<h2>Inner Join</h2>

Created a SQL query on MariaDB to join two tables focusing on the intersection of two tables. We only care about rows that have corresponding values in both.

<b>"Employees” Table</b>

![Screenshot 2024-08-03 at 9 20 07 PM](https://github.com/user-attachments/assets/b2c7f11f-4a41-4bc6-b61e-5035917a22e5)

<b>"Machines” Table</b>

![Screenshot 2024-08-03 at 9 20 16 PM](https://github.com/user-attachments/assets/450aac91-a7b8-4ab5-aeea-812590c99ecf)

This is the query that produces username, operating system, and employee ID from both
tables. The username is from one of the tables and so is the operating system. For the table
that can be found on both, we use <mark>“table.column”</mark> format to avoid ambiquity. In this case it is
the employee table (employee ID). There are 185 usernames with respective
operating systems and device IDs. Other variations can be found in the next pages of
Join.

![Screenshot 2024-08-03 at 9 20 30 PM](https://github.com/user-attachments/assets/7116f718-836f-4cd7-b102-f69563d8e093)

This query will produce username, employee ID, operating system, device ID and their
respective office.

![Screenshot 2024-08-03 at 9 20 41 PM](https://github.com/user-attachments/assets/a436cb22-1a16-4c89-a3d0-7ab11780490b)
![Screenshot 2024-08-03 at 9 20 47 PM](https://github.com/user-attachments/assets/9e66e956-6f16-48bd-ba71-d8947ff27920)

<h2>Return More Data</h2>

<mark>LEFT JOIN</mark>. The results will include all records from one or the other table. We link
these tables using the <mark>common device_id</mark> column. In a left join, all records after <mark>FROM</mark> and
before <mark>LEFT JOIN</mark> are included in the result. In this case, all records from the <mark>machines</mark>
table are included, whether they are assigned to the <mark>employees</mark> table or not.

![Screenshot 2024-08-03 at 9 20 57 PM](https://github.com/user-attachments/assets/1a57e75b-9d36-4d72-9532-805839c0c8aa)

<mark>RIGHT JOIN</mark>. The results will include all records from one or the other table. We link
these tables using the <mark>common device_id</mark> column. In a right join, all records after <mark>FROM</mark> and
before <mark>RIGHT JOIN</mark> are included in the result. In this case, all records from the <mark>machines</mark>
table are included, whether they are assigned to the <mark>employees</mark> table or not.

![Screenshot 2024-08-03 at 9 21 10 PM](https://github.com/user-attachments/assets/eab4fbb1-aa74-4369-adf3-a895a4dc34e9)

Both produced 200 rows each, however in the process, some data are written <mark>NUL</mark> due to
types of <mark>JOIN</mark>.

<h2>Summary</h2>

Wrote queries to join two tables in three different scenarios: Inner Join, Left Join, and Right
Join.
