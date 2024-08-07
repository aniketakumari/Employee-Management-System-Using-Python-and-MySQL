# Employee Management System Using Python and MySQL

## Project Overview
This project is an Employee Management System built using Python with a MySQL database as the backend. The system allows users to manage employee records effectively, performing CRUD (Create, Read, Update, Delete) operations. It offers functionalities to add new employees, remove existing employees, promote employees by increasing their salary, and display all employee records. The primary advantage of this system is that it stores data in a persistent database, ensuring that information is retained even after the program is closed.

## Features:
1. Add Employee: Insert a new employee record into the database.
2. Remove Employee: Delete an existing employee record from the database.
3. Promote Employee: Increase an employee's salary and update their record.
4. Display Employees: Retrieve and display all employee records from the database.

## Getting Started
To get started with the Employee Management System, you'll need to have Python and MySQL installed on your system. You'll also need the MySQL Connector package to establish a connection between Python and the MySQL database.

## Prerequisites
1. Python 3.x: Make sure Python is installed on your system. You can download it from Python's official website.
2. MySQL Server: Ensure that MySQL is installed and running. You can download it from MySQL's official website.
3. MySQL Connector: Install the MySQL Connector for Python using the following command:

## Installation
The recommended way to install Connector/Python is via pip.

Make sure you have a recent pip version installed on your system. If your system already has pip installed, you might need to update it. Or you can use the standalone pip installer.

The classic API can be installed via pip as follows:

```
$ pip install mysql-connector-python
```
## Database Setup
Create the MySQL Database:

Open your MySQL Command Line Client or MySQL Workbench and create a new database named emp:

```
CREATE DATABASE emp;
Create the employees Table:
```

Switch to the emp database and create the employees table:
```
USE emp;
```
```
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    post VARCHAR(50),
    salary DECIMAL(10, 2)
);
```

Database Connection:

The script starts by establishing a connection to the MySQL database using the function.
```
mysql.connector.connect()
```
## Employee Management Functions:

* check_employee(employee_id): Verifies if an employee exists in the database.
* add_employee(): Adds a new employee to the database.
* remove_employee(): Removes an existing employee from the database.
* promote_employee(): Increases an employee's salary and updates the record in the database.
* display_employees(): Fetches and displays all employee records from the database.

  
## Menu Interface:

The menu() function provides a simple command-line interface for users to interact with the Employee Management System.

```
# Function to display the menu
def menu():
    while True:
        print("\nWelcome to Employee Management Record")
        print("Press:")
        print("1 to Add Employee")
        print("2 to Remove Employee")
        print("3 to Promote Employee")
        print("4 to Display Employees")
        print("5 to Exit")
        
        ch = input("Enter your Choice: ")

        if ch == '1':
            add_employee()
        elif ch == '2':
            remove_employee()
        elif ch == '3':
            promote_employee()
        elif ch == '4':
            display_employees()
        elif ch == '5':
            print("Exiting the program. Goodbye!")
            break
        else:
            print("Invalid Choice! Please try again.")
```
### How It Works

1. Add Employee: The user inputs the employee's ID, name, post, and salary. The system checks if the employee already exists before adding the new record to the database.
2. Remove Employee: The system removes the employee record based on the employee ID after confirming that the employee exists in the database.
3. Promote Employee: The system allows the user to input a salary increment for an employee. The system updates the employee’s salary in the database accordingly.
4. Display Employees: The system fetches all records from the employees table and displays each employee's details.

## Future Scope
1. Expand Functionality: Add more features like employee performance reviews, department management, or leave tracking.
2. Web Interface: Build a web-based interface using frameworks like Flask or Django to make the system accessible over the web.
3. Enhanced Security: Implement user authentication and authorization to protect sensitive employee data.
4. Analytics Dashboard: Integrate data analytics tools to provide insights into employee metrics like salary distribution, promotion rates, and department performance.
   
This Employee Management System is a scalable project that can be expanded and modified according to your needs. By connecting Python with MySQL, you have created a robust, persistent system for managing employee data.
