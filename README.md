# Home-Credit-Default-Risk-Database-Data-Models-and-Query-Languages
A structured SQL database designed for analyzing home credit default risks, ensuring efficient storage, retrieval, and assessment of financial data. Built using PostgreSQL with normalized tables for better data integrity and performance.

# Home Credit Default Risk Database

This project involves the creation of a database related to home credit default risk. The goal is to design, load, and manage a database that is useful in the banking and home credit industry. The database can be utilized by:

- Banks by Loan Officers
- Data Analysts
- Database Administrators

## Database Entities
The database consists of six tables:

- **Bureau** - Contains information about previous credit history reported by credit bureaus for clients.
- **Bureau Balance** - Stores monthly balance information for each credit reported by credit bureaus.
- **Credit Card Balance** - Maintains monthly balance information for credit cards.
- **Installment Payments** - Records payments made for previous installments.
- **POS CASH Balance** - Stores monthly balance information for cash loans.
- **Previous Application** - Contains information about past loan applications.

During the database creation, we tested queries, ensured compliance with BCNF principles, and applied database design best practices. The data in the tables was generated using the Faker library in Python.

## Database Creation Process

### 1. Database Creation
- Created a database named **Home Risk**.

### 2. Creating Tables and Schema
- Used **CREATE TABLE** queries to set up tables.
- Defined **Primary Key** and **Foreign Key** constraints for each table.

### 3. Ensuring BCNF Compliance
- Decomposed the **Installment Payments** table into **Installment Payments Details** and **Installment Payments Header** to eliminate BCNF violations.
- Applied database design principles to ensure normalization.

### 4. Data Generation
- Used **Pandas** and **Faker** libraries to generate realistic data.
- Created meaningful values for each attribute.
- Ensured referential integrity between tables as per the E/R Diagram.
- Exported generated data to **.csv** files.

### 5. Data Import
- Imported data into the database using **PgSQL tools**.

## Tools & Technologies Used
- **PostgreSQL** for database management.
- **Python** for data generation using Faker.
- **Pandas** for data handling.
- **PgSQL tools** for database operations.




