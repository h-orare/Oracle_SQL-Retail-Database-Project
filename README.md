This project focused on the practical applications of database systems in a typical organization and how they support business operations. 

To achieve this goal.
1.	I designed and developed Oracle database tables holding data for Employees, Customers, Orders, Products, Invoices, Payroll for a fictional retail business company.
2.	Developed E-R relationships between and among those tables with necessary constraints to ensure referential integrity, consistency and validity of data they hold. I then ran DDL scripts to create these tables in Oracle
3.	From this site(https://www.mockaroo.com), I generated dummy data sets and imported the data into those tables in Oracle

Business Use Cases:
1.	Deriving Business Insights on Sales Performance
Developed and scripted various Stored Procedures that
-	Check stock levels for all products. When executed, the procedure issues an alert if any product stock level falls below a minimum_stock_quantity-
-	Display customers who purchased the most in terms of value for a given trading period. This insight can be valuable if a company wishes to initiate a reward program for its customers
- Determine and display product categories with highest gross margins. An insight that can inform decisions on product positioning, marketing campaigns etc

2.	Data Security, Access & Governance
Developed various data security and access measures as outline below.
- A view for the employees table that abstracts employee details like salary and other personal information from access by any other user other than HR Manager. This is to protect and restrict sensitive data
- A trigger that logs details into a table called employee_audit_table whenever an INSERT, UPDATE or DELETER action is performed on the employee table. This ensures security audit trail for all actions performed on that table object
- Created users, roles and assigned both System and Object privileges to appropriate users. In this example, I created a role called marketing_interns which I assigned to interns currently working in the Marketing Department. This role allowed READ only access to Customers, Orders, Products and Invoices tables only.
- Recently the company created a staff welfare initiative and nominated a group of 5 employees from different departments. Among other initiatives, the group has decided to be sending surprise birthday gifts to employees’ residence addresses. As such, this group needs access to the employees table to be able to obtain data on where each employee lives. To protect other sensitive data in employees table, I granted READ ONLY access to employee_view table that only gives them employee names, day & month of birth and residence address only. All other details abstracted.
