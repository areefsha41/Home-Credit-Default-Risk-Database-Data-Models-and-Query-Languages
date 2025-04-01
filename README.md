# Home-Credit-Default-Risk-Database-Data-Models-and-Query-Languages
A structured SQL database designed for analyzing home credit default risks, ensuring efficient storage, retrieval, and assessment of financial data. Built using PostgreSQL with normalized tables for better data integrity and performance.

# Home Credit Default Risk Database

## Project Overview
This project focuses on designing, building, and populating a database to analyze home credit default risks. By following solid database design principles, we ensure the data remains structured, normalized, and consistent. The database is intended for use by banks, loan officers, data analysts, and database administrators to help assess and manage credit risk.

## Use Case
This database is designed to store and manage financial data related to home credit, including past credit history, credit card balances, installment payments, and loan applications. It can be used for:
- Evaluating credit risk
- Assessing loan applications
- Analyzing payment behavior trends

## Database Schema
The database consists of six main tables:
1. **Bureau** - Stores clients' previous credit information reported by credit bureaus.
2. **Bureau Balance** - Maintains monthly balance details for each credit reported by bureaus.
3. **Credit Card Balance** - Tracks monthly balance details for credit cards.
4. **Installment Payments** - Logs payments made for prior installments.
5. **POS CASH Balance** - Stores monthly balance details for cash loans.
6. **Previous Application** - Contains information about past loan applications.

## Database Design & Normalization
- The database was developed using best practices in relational database design.
- To maintain efficiency, normalization was enforced, ensuring compliance with **Boyce-Codd Normal Form (BCNF)**.
- The **Installment Payments** table was split into **Installment Payments Details** and **Installment Payments Header** to remove BCNF violations.

## Data Generation & Import
- **Simulated Data:** The `Faker` library in Python was used to generate realistic financial data.
- **Data Storage:** Generated data was saved as `.csv` files.
- **Data Import:** These `.csv` files were then imported into the PostgreSQL database.

## Implementation Steps
1. **Database Creation:**
   - A PostgreSQL database named `Home_Risk` was set up.
2. **Table Creation:**
   - Tables were designed with appropriate `PRIMARY` and `FOREIGN KEY` constraints to enforce relationships.
3. **Normalization:**
   - Schema was checked for BCNF compliance, with decomposition applied where necessary.
4. **Data Generation:**
   - Used `pandas` and `Faker` to create synthetic but realistic data.
5. **Data Import:**
   - The generated `.csv` files were imported using PostgreSQL's `COPY` or `INSERT` commands.

## Technologies Used
- **SQL (PostgreSQL)** for database design and querying.
- **Python (Pandas, Faker)** for generating sample data.
- **PgAdmin / PSQL CLI** for managing the database.

## Getting Started
1. Set up a PostgreSQL database and create tables using the provided schema.
2. Generate and import data using the included scripts.
3. Run SQL queries to analyze the data.

## Future Enhancements
- Add stored procedures to automate risk assessment.
- Integrate machine learning models to predict loan defaults.
- Optimize indexing strategies to enhance query performance.



