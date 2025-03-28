# SQL Documentation

## What is SQL?
Structured Query Language (SQL) is a standard language used to communicate with relational databases. It allows users to store, retrieve, manipulate, and manage data efficiently.

## Why Use SQL?
- **Data Management:** Helps in handling large amounts of structured data.
- **Querying Data:** Allows retrieving specific data using SELECT queries.
- **Data Integrity:** Ensures accuracy and consistency of data.
- **Scalability:** Used in small applications and enterprise-level databases.

## How to Install SQL Server
### **Windows**
1. Download **SQL Server Express** from [Microsoft's official site](https://www.microsoft.com/en-us/sql-server/sql-server-downloads).
2. Run the installer and follow the setup wizard.
3. Install **SQL Server Management Studio (SSMS)** for a user-friendly interface.
4. Open SSMS, connect to the database engine, and start using SQL.

### **Linux**
1. Add the Microsoft SQL Server repository:
   ```sh
   sudo wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
   sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2022.list)"
   ```
2. Install SQL Server:
   ```sh
   sudo apt update
   sudo apt install -y mssql-server
   ```
3. Run setup and configure:
   ```sh
   sudo /opt/mssql/bin/mssql-conf setup
   ```
4. Install SQL Server command-line tools:
   ```sh
   sudo apt install -y mssql-tools unixodbc-dev
   ```
5. Connect using:
   ```sh
   sqlcmd -S localhost -U SA -P '<YourPassword>'
   ```

## Basic SQL Commands
### **Creating a Database**
```sql
CREATE DATABASE MyDatabase;
```

### **Creating a Table**
```sql
CREATE TABLE Employees (
    ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Age INT,
    Department VARCHAR(50)
);
```

### **Inserting Data**
```sql
INSERT INTO Employees (ID, Name, Age, Department)
VALUES (1, 'John Doe', 30, 'HR');
```

### **Retrieving Data**
```sql
SELECT * FROM Employees;
```

### **Updating Data**
```sql
UPDATE Employees
SET Age = 31
WHERE ID = 1;
```

### **Deleting Data**
```sql
DELETE FROM Employees
WHERE ID = 1;
```

## Best Practices
- Always use **primary keys** for unique identification.
- Use **indexes** to improve query performance.
- Normalize your database to avoid redundancy.
- Use **transactions** to maintain data consistency.

This documentation serves as a foundation for understanding SQL. More advanced topics like stored procedures, joins, and indexing will be covered in additional sections.

