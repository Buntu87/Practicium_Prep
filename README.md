# Practicium_Prep
Below is the IT_Gear_Project with an ERD Design
ERD DESCRIPTION

Entities:
- STOCK (PK: STOCK_ID)
- CUSTOMER (PK: CUST_ID)
- REPAIRS (PK: REPAIR_ID)
- SALES (PK: SALES_NUM)

Relationships:
- SALES references STOCK (Many-to-One)
- SALES references CUSTOMER (Many-to-One)
- SALES references REPAIRS (Many-to-One)
The zip fie contains the following
An IT Gear Dealer Database, and created tables (STOCK TABLE,CUSTOMER TABLE,REPAIRS TABLE,SALES TABLE). Thus the following data inserts where allocated to tables(INSERT INTO STOCK VALUES (12345,'Desktop','Proline K100','Acer');
INSERT INTO STOCK VALUES (54321,'Laptop','J55','Mecer');
INSERT INTO STOCK VALUES (78945,'Server','HP9000','Samsung');
INSERT INTO STOCK VALUES (98754,'Laptop','Aspire 450','HP');
INSERT INTO STOCK VALUES (55311,'Notebook','L920','Lenovo');

INSERT INTO CUSTOMER VALUES ('C115','Jeff','Willis','3 Main Road','0821253659');
INSERT INTO CUSTOMER VALUES ('C116','Andre','Watson','13 Cape Road','0769658547');
INSERT INTO CUSTOMER VALUES ('C117','Wallis','Smith','3 Mountain Road','0863256574');

INSERT INTO REPAIRS VALUES (1,'HD defragmentation',TO_DATE('15/JUL/2023','DD/MON/YYYY'),2);
INSERT INTO REPAIRS VALUES (2,'RAM module replaced',TO_DATE('18/JUL/2023','DD/MON/YYYY'),3);

INSERT INTO SALES VALUES (101,TO_DATE('27/JUL/2023','DD/MON/YYYY'),1700,98754,'C115',1);
Ultimatly (Question 1: ERD & Database Setup

This task involved designing and implementing a fully functional Oracle database based on the IT Gear Dealer case study. The database was structured into four main entities: STOCK, CUSTOMER, REPAIRS, and SALES, each representing key business operations. Primary keys were defined to uniquely identify each record, while foreign keys were used in the SALES table to establish relationships with the other entities, ensuring referential integrity. Appropriate constraints such as data types and key relationships were applied to maintain data consistency and accuracy. An Entity Relationship Diagram (ERD) was also created to visually represent the database structure, clearly illustrating the one-to-many relationships between CUSTOMER and SALES, STOCK and SALES, and REPAIRS and SALES. This ensured that the database design aligns with real-world business rules and supports efficient data management.

Question 2: Query Time Taken to Complete Repairs

In this task, a SQL query was written to retrieve specific repair-related information by joining multiple tables. The query combines customer names, repair work descriptions, repair dates, and the number of hours taken to complete each repair. This was achieved by joining the CUSTOMER, SALES, and REPAIRS tables using their respective keys. A filtering condition was applied to only display records where the repair duration was less than three hours, demonstrating the use of the WHERE clause for conditional data retrieval. This query highlights how relational databases can efficiently combine and filter data from multiple sources to generate meaningful business insights.

Question 3: Query Sales Made (PL/SQL)

This task required the use of PL/SQL to process and display sales data dynamically. A PL/SQL block was created with variables to store customer ID, stock type, and sales amount. A cursor loop was used to iterate through records retrieved from a SELECT statement that joins the SALES and STOCK tables. The condition ensured that only sales with an amount less than R1500 were displayed. The output was printed using DBMS_OUTPUT, demonstrating procedural control and output formatting in PL/SQL. This task illustrates how PL/SQL enhances SQL by allowing logic, iteration, and conditional processing within database operations.

Question 4: Query Calculate Commission

In this task, a PL/SQL program was developed to calculate commission based on sales amounts according to defined business rules. A loop was used to process each sales record, and conditional statements (IF, ELSIF, ELSE) were applied to determine the correct commission percentage. Sales below R1000 earned 5%, those between R1000 and R1499 earned 10%, and sales of R1500 or more earned 15%. The calculated commission, along with other relevant details such as customer ID, stock ID, and sales number, was displayed using DBMS_OUTPUT. This task demonstrates the use of decision-making structures in PL/SQL to implement real-world business logic within a database system.

Question 5: Create View

This task involved creating a database view named Repair_View to simplify complex queries. The view combines data from multiple tables (CUSTOMER, SALES, and REPAIRS) to display a consolidated result including customer name, stock ID, repair date, and repair work performed. The CREATE OR REPLACE VIEW statement ensures that the view can be updated if needed. By querying the view, users can easily access relevant information without needing to write complex join statements repeatedly. This improves efficiency, readability, and security by restricting direct access to underlying tables.

Question 6: Create Trigger

In this task, a database trigger named Sales_Entry was created to enforce data integrity rules. The trigger is executed before any INSERT or UPDATE operation on the SALES table. It checks whether the sales amount entered is less than zero and prevents invalid data from being stored by raising an application error. This ensures that all sales records maintain valid, non-negative values. A test statement was included to demonstrate the trigger’s functionality. This task highlights the importance of using triggers to automate validation and enforce business rules at the database level.

Question 7: Create Stored Procedure

This task required the creation of a stored procedure named sp_customer_details, which accepts a sales number as input and retrieves corresponding customer details. The procedure uses a SELECT statement to join CUSTOMER and SALES tables and fetch the customer ID, first name, surname, and contact number. A loop is used to display the results using DBMS_OUTPUT. Exception handling was included to manage cases where no matching data is found, ensuring robustness. The procedure can be executed independently, promoting code reusability and modular database design.

Question 8: Create Function

In this task, a user-defined function named fn_IT_Gear was created to return meaningful information based on a sales number input. The function retrieves and combines multiple data elements such as customer ID, customer name, sales amount, and stock type into a single output string. Exception handling was implemented to manage scenarios where no data is found. The function can be called within SQL statements, demonstrating how functions extend database capabilities by encapsulating reusable logic and returning computed results.

Question 9: Create GUI

This task involved designing a graphical user interface (GUI) to simulate interaction with the database procedures and functions. The GUI provides menu options that allow users to select and view outputs from the stored procedure and function created earlier. Although the GUI is not connected to the database, it demonstrates how a front-end application can be structured to interact with backend logic. This task emphasizes the importance of user-friendly interfaces in software systems and shows how database results can be presented visually.

Question 10: Database Security Mini-Presentation

This task focused on identifying and explaining methods to ensure database security within the IT Gear Dealer system. Key measures include implementing user authentication and role-based access control to restrict unauthorized access, encrypting sensitive customer data to protect confidentiality, using secure backups to prevent data loss, applying input validation to prevent SQL injection attacks, and enabling auditing to monitor database activities. These strategies are crucial in protecting sensitive business and customer information. The discussion also links these security practices to the case study, emphasizing their relevance in maintaining trust, compliance, and operational integrity.                                                                                                                                                                                 Thus concluding the assessment
