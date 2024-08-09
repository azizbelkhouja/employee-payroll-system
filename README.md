# employee-payroll-system

This project is a simple Java application that manages a payroll system. It includes the ability to handle both full-time and part-time employees, calculate their salaries, and manage employee records.

## Features

- **Employee Management**: Add and remove employees from the payroll system.
- **Salary Calculation**: Automatically calculate salaries for both full-time and part-time employees.
- **Employee Display**: Print out the details of all employees, including their calculated salaries.

## Classes

### `Employee`

This is an abstract class that represents a generic employee. It includes:

- **Attributes**:
  - `name`: The name of the employee.
  - `id`: The unique ID of the employee.
- **Methods**:
  - `getName()`: Returns the name of the employee.
  - `getId()`: Returns the ID of the employee.
  - `calculateSalary()`: Abstract method to be implemented by subclasses to calculate the employee's salary.
  - `toString()`: Returns a string representation of the employee, including their name, ID, and salary.

### `FullTimeEmployee`

This class extends the `Employee` class and represents a full-time employee. It includes:

- **Attributes**:
  - `monthlySalary`: The monthly salary of the employee.
- **Methods**:
  - `calculateSalary()`: Returns the monthly salary.

### `PartTimeEmployee`

This class extends the `Employee` class and represents a part-time employee. It includes:

- **Attributes**:
  - `hoursWorked`: The number of hours worked by the employee.
  - `hourlyRate`: The hourly rate of the employee.
- **Methods**:
  - `calculateSalary()`: Returns the total salary based on hours worked and the hourly rate.

### `PayrollSystem`

This class manages a list of employees and provides functionalities to add, remove, and display employees. It includes:

- **Attributes**:
  - `employeeList`: A list of employees in the payroll system.
- **Methods**:
  - `addEmployee(Employee employee)`: Adds an employee to the payroll system.
  - `removeEmployee(int id)`: Removes an employee from the payroll system based on their ID.
  - `displayEmployees()`: Prints out the details of all employees in the payroll system.

## Main Class

The `Main` class is the entry point of the application. It demonstrates the following:

- Adding full-time and part-time employees to the payroll system.
- Displaying initial employee details.
- Removing an employee from the payroll system.
- Displaying the remaining employee details after removal.

## How to Run

1. Compile the Java files:

    ```bash
    javac Main.java
    ```

2. Run the application:

    ```bash
    java Main
    ```

## Example Output

```plaintext
Initial Employee Details:
Employee [name=Steve Jobs, id=101, salary=5000.0]
Employee [name=Enzo Ferrari, id=102, salary=450.0]

Removing Employee...

Remaining Employee Details:
Employee [name=Enzo Ferrari, id=102, salary=450.0]
