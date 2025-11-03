# SQL-Server-to-MySQL-Data-Migration-Project
This project demonstrates how to migrate data dynamically from SQL Server (SSMS) to MySQL using Python. It features dynamic table creation based on SQL Server schema, data type mapping, and row migration, making it ideal for database administrators and developers.
Features

Connects to SQL Server using pyodbc and MySQL using pymysql.

Dynamically retrieves all user tables from SQL Server.

Converts SQL Server data types to MySQL-compatible types.

Creates tables in MySQL with proper column definitions and primary keys.

Migrates table data with error handling and logging of failed rows.

Provides a migration summary with total tables and rows migrated.

Prerequisites

Python 3.x

SQL Server (Express or Full)

MySQL Server

Python packages:

pip install pyodbc pymysql
Project Structure
SQLServer_to_MySQL_DataMigration/
│
├── migration.py       # Main Python migration script
├── requirements.txt   # Python dependencies
├── sample_data/       # Optional: SQL scripts to create sample tables
│   ├── create_tables.sql
│   └── insert_data.sql
└── docs/              # Optional: Screenshots or workflow diagrams
How to Run

Clone the repository:

git clone https://github.com/<your-username>/SQLServer_to_MySQL_DataMigration.git
cd SQLServer_to_MySQL_DataMigration

Update database connection settings in migration.py:

SQL Server:

SERVER = 'TABISH\\SQLEXPRESS04'
DATABASE = 'Tabish'

MySQL:

host='localhost'
user='root'
password='root'
database='newdb'

Run the migration script:

python migration.py

Check the output in MySQL to verify tables and data.

Sample Output
Connected successfully!

Found 5 table(s) to migrate:

  • [dbo].[Cars] - 100,000 rows
  • [dbo].[CarTransactions] - 150,000 rows

Starting migration...

[1/5] Migrating: [dbo].[Cars]
  ✅ Table created
  📦 Migrating 100,000 rows...
  ✅ Migrated 100,000/100,000 rows

Migration summary:
✅ Successfully migrated: 5/5 tables
📊 Total rows migrated: 500,000
Optional Enhancements

Include a workflow diagram in docs/ showing SQL Server → Python → MySQL.

Add logging to a file for tracking errors and migration progress.

Include sample SQL scripts in sample_data/ for easy testing.

Author

MD Tabish Kalim
SQL Developer | Python Enthusiast | Data Migration Specialist

License

This project is licensed under the MIT License.

---

If you want, I can also **create a polished `requirements.txt` and a sample GitHub repo README with badges and links** so your project looks fully professional on GitHub.  

Do you want me to do that next?
