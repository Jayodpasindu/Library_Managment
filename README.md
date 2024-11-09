# README: Database Configuration and Queries

This document provides instructions for updating the database password in the Hibernate configuration file (`hibernate.cfg.xml`) and informs where to find the database queries.

## Updating Database Password

1. **Locate the Configuration File**  
   The Hibernate configuration file, `hibernate.cfg.xml`, is located in the project’s resources directory, usually under `src/main/resources`. This file contains the database connection settings.

2. **Change the Database Password**  
   To update the password, find the following line in `hibernate.cfg.xml`:
   ```xml
   <property name="hibernate.connection.password">password</property>
   ```
   Replace `password` with the actual password for the MySQL database, and save the file.

3. **Restart the Application**  
   After updating the password, restart the application to apply the changes.

## Database Queries

All SQL queries required for setting up or modifying the database structure are stored in a separate SQL file named `sql`.

### Location of SQL File
The `sql` file is located in the `src/main/resources/sql` directory. This file includes:
- Table creation statements
- Initial data insertions
- Additional queries necessary for database setup

### Running the SQL File
To execute the queries in `sql`:
1. Open your MySQL client or command line.
2. Run the following command:
   ```bash
   mysql -u root -p library_management < src/main/resources/sql
   ```
   Replace `library_management` with your database name if it's different.

---

By managing SQL queries in `src/main/resources/sql`, you can easily apply initial data and schema updates as needed. Be sure to check and update this file if there are any changes to the database structure.
