#### Introduction: <br>
Create a database that will be able to assist in business growth with expansion plans. The database language is SQL Oracle. The database must have at least five entities as well as five attributes. The database must be scalable due to expansions resulting in the need of more data input within the database. Receiving entity will only be expected to use SQL Oracle DML once the database has been established and delivered. 

Overview:
Candid.inc is a startup technical company that is looking to establish itself globally. Candid.inc is in need of a data model that will assist in global reach. The original data model acquired by Candid.inc is no longer relevant for the new direction of the company. Candid.inc will require a new data model that will scale with the future of the company. Since this is a new venture for Candid.inc, third party contributors will be necessary to ensure that global reach is possible for the business. Candid.inc will need to be able to keep track of cost, projects and internal business related entities.

Assumptions:
The database will be based on the relationship that the company is the main table. This is due to the fact that Candid.inc is solely interested in productivity and costs of the business. In this relationship assumption the partner companies will only be working with Candid.inc on projects to expand the business that internal entities can not handle due to current workloads. Candid.inc has been around for a while, however, this venture is new along with the resources associated with it. Database tables, data manipulations and queries will be executed one at a time with multiple executions opposed from a single unit execution. 

#### Statement of Work <br>
Scope:
To establish a database that will serve Candid.inc as a resource to track and manage business expansion. The database will also keep track of finances in relation to internal and external business entities. All business partners will be able to verify their approval status as well as the approval status for active projects they are assigned. All database information can be manipulated by internal parties within Candid.inc.

Deliverables:
Populated Oracle SQL code output for the database using test examples will be delivered before purchase agreement in case changes need to be made. On agreement theOracle SQL DDL code will be delivered through a shared drive with authentications to ensure integrity and confidentiality. 

Timeline:
Creation of the database will take approximately one year from start date. During this phase  updates will be provided quarterly. Payment of twenty-five percent will be due at the approval of each submission. 
 
#### Requirements and Definition <br>
Entity and Attribute Description:  <br>
Company in the head of the organization that makes the final decisions for the business.  <br>
Company_ID is the primary key and is used for approvals and financial references.  <br>
Name is used to identify the company. Address shows the location of the company.  <br>
DSN_Phone is the land line voice service number to the company.  <br>
Emergency_Phone is the number to call in case of emergency.  <br>
Department is the entity within the company that is responsible for different services.  <br>
Dept_ID is the primary key and is used to isolate one department. <br>
Name is associated with service of the department to make the department's service identifiable.  <br>
Phone is the land line voice service number to the department directly. <br>
Budget is the financial responsibility the company has to allocate to each department for the duration of the company.  <br>
Employee_Count is the number of employees dedicated to the department.  <br>
Employee are the professionals that are employed at the company.  <br>
Employee_ID is the primary key and is used to isolate each employee and can be used to verify integrity.  <br>
Name is the name of the professional that works for the company. <br>
Address is the home location of the employee.  <br>
Phone is the personal number that is used to contact the employee directly.  <br>
Start_Date is reflecting the date the employee was hired for the company. <br>
Cost is the additional financial resources the company has for additional tasks. <br>
The Cost_ID is the primary key and is associated with the project or the partner company. <br>
Approval_Status is the decision by the company if the budget has been approved.  <br>
Variable_Budget is the extra resources the company has for an approved Cost_ID.  <br>
The Fixed_Budget is the agreed-on budget based on everything running smoothly. <br>
Approved_Date is the date that the budget has been approved.  <br>
Partner_CO is the additional company that provides services as needed on a contract basis.  <br>
Partner_ID is the unique identifying ID for each partner company.  <br>
Name is the name of the partnered company.  <br>
DSN_Phone is the land line voice service number to the partnered company.  <br>
FK_Cost_pk_Cost_ID is the foreign key and provides the approved budget for the provided service from the partner company. <br>
FK_Project_pk_Project_ID is the other foreign key and is the project reference number that the partnered company has been hired to provide services. <br>
Project is additional tasks that deviates from the normal daily company routine.  <br>
Project_ID is the unique number that is associated with additional projects and is a primary key.  <br>
Name is the name of the project used to differentiate the projects to stakeholders.  <br>
StartDate is the date the project operations start. <br>
EndDate is the projected completion date of the project.  <br>
FK_Cost_pk_Cost_ID is the cost ID that is associated with each project. <br>
 
#### Detailed Design <br>
Relationship and Cardinality Description:
Relationship: “Works” between COMPANY and DEPARTMENT
Cardinality: 1:M between COMPANY and DEPARTMENT
Business rule: A company can have many departments; a department can only have one company.

Relationship: “Works” between COMPANY and PARTNER_CO
Cardinality: Optional 1:M between COMPANY and PARTNER_CO
Business rule: A company partner many partner companies; a partner company can partner with one company.

Relationship: “Works” between DEPARTMENT and EMPLOYEE
Cardinality: 1:M between DEPARTMENT and EMPLOYEE
Business rule: A department can have many employees; an employee can only have one department.

Relationship: “Authorized” between COMPANY and COST
Cardinality: Optional 1:M between COMPANY and COST
Business rule: A company can have many costs; costs can only have one company.

Relationship: “Appointed” between PARTNER_CO and PROJECT
Cardinality: 1:M between PARTNER_CO and PROJECT
Business rule: A partner company can have many projects; a project can only have one partner company.

Relationship: “Appointed” between DEPARTMENT and PROJECT
Cardinality: Optional 1:M between DEPARTMENT and PROJECT
Business rule: A department can have many projects; a project can only have one department.

Relationship: “Authorized” between PROJECT and COST
Cardinality: 1:M between PROJECT and COST
Business rule: A project can have many costs; cost can only have one project.

#### Entity Relationship Diagram (ERD)

![Image_Alt](https://github.com/KevinBL-DBA/Projects/blob/eb870799816865fcc5dae1dce5a6eb4001a390f6/ERD.jpg)

#### References: <br>

Elmasri, R., & Navathe, S. (n.d.). Fundamentals of Database Systems elmasri navathe 3rd 
edition. Retrieved March 30, 2023, from 
http://survey3.knbs.or.ke/upload/open.php?article=fundamentals-of-database-systems-el
masri-navathe-3rd-edition-pdf&code=a77ca38d60101fba469a7f867fd85f0b
Dewiyanti, S. (2021, November 17). Types of budget for Government. Accounting. 
Retrieved March 30, 2023, from 
https://accounting.binus.ac.id/2021/11/17/types-of-budget-for-government/
Geeks. (2020, January 6). Top 7 database you must know for software development projects. 
GeeksforGeeks. Retrieved March 30, 2023, from 
https://www.geeksforgeeks.org/top-7-database-you-must-know-for-software-development
-projects/
Geeks. (2023, March 10). The problem of redundancy in database. GeeksforGeeks. Retrieved 
March 30, 2023, from 
https://www.geeksforgeeks.org/the-problem-of-redundancy-in-database/
Gutmans, A. (2022, November 9). Google cloud brandvoice: Cloud databases: The secret 
advantage of digital innovators. Forbes. Retrieved March 30, 2023, from 
https://www.forbes.com/sites/googlecloud/2021/09/23/cloud-databases-the-secret-advant
age-of-digital-innovators/
IBM. (n.d.). SQL Server database privileges. SQL Server Database Privileges. Retrieved March 
30, 2023, from 
https://www.ibm.com/docs/en/baw/19.x?topic=privileges-sql-server-database
Microsoft. (n.d.). What are databases? – what is a database?: Microsoft Azure. What Are 
Databases? – What is a Database? | Microsoft Azure. Retrieved March 30, 2023, from 
https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-are-databa
ses/ 
