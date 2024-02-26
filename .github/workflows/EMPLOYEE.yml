import pandas as pd
from sqlalchemy import create_engine

# Data Retrieval from Excel File
excel_data = pd.read_excel('/Users/mani/Downloads/Employee.xlsx')

# MySQL Database Integration
engine = create_engine('mysql://user:password@localhost/db_name')
excel_data.to_sql('Employee', con=engine, if_exists='replace')

# Data Storage and CRUD Operations
# Create
engine.execute("INSERT INTO Employee VALUES (...)")

# Read
result = engine.execute("SELECT * FROM Employee")

# Update
engine.execute("UPDATE Employee SET ... WHERE ...")

# Delete
engine.execute("DELETE FROM Employee WHERE ...")

# Data Filtering Scripts
# Retrieve data for employees in Engineering department
engineering_data = pd.read_sql("SELECT * FROM Employee WHERE Department='Engineering'", con=engine)

# Retrieve data for employees with Salary between 50000 and 75000
salary_data = pd.read_sql("SELECT * FROM Employee WHERE Salary BETWEEN 50000 AND 75000", con=engine)

# Retrieve data for employees with First Name containing 's' and Department as 'HR'
filtered_data = pd.read_sql("SELECT * FROM Employee WHERE First_Name LIKE '%s%' AND Department='HR'", con=engine)
