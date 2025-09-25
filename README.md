# Vithyarthi-java-project-

# Campus Course & Records Manager (CCRM)

The Campus Course & Records Manager (CCRM) is a console-based application designed to manage students, courses, enrollments, and grades. The project serves as a comprehensive demonstration of various fundamental and advanced Java programming concepts, including Object-Oriented Programming (OOP) principles, modern Java 8+ features, and common design patterns.

## Features

* **Student Management**: Add, list, update, and view student transcripts.
* **Course Management**: Add new courses, view a sorted list of all courses, and search or filter courses by keyword.
* **Enrollment & Grades**: Enroll students in courses and assign grades to their enrollments.
* **Data Utilities**: Import data from CSV files, export data to CSV files, and create timestamped backups of data.
* **Reports**: Generate reports, such as a GPA distribution report for all students.

## Technologies & Key Java Concepts Demonstrated

This project is built using **Java SE** and showcases a variety of programming concepts and design patterns.

### Object-Oriented Programming (OOP)
* **Inheritance**: The `Student` and `Instructor` classes extend the `Person` base class.
* **Encapsulation**: Data fields are private with public getters and setters, for example in the `Person` class.
* **Polymorphism**: The `getProfile()` method is overridden in subclasses like `Student` and `Instructor`, demonstrating polymorphic behavior.

### Design Patterns
* **Singleton**: The `AppConfig` class uses the Singleton pattern to ensure a single, globally accessible configuration instance.
* **Builder**: The `CourseBuilder` static nested class allows for the flexible and readable creation of `Course` objects.

### Modern Java (Java 8+)
* **Stream API**: Used extensively for data processing, filtering, and aggregation. Examples include `CourseService.searchCourses()` and `ReportsMenu.generateGpaDistributionReport()`.
* **Lambdas & Functional Interfaces**: `Comparator` instances in the `Comparators` utility class are implemented using lambdas.
* **Optional**: The `EnrollmentService` uses `Optional` to handle the potential absence of an enrollment record when assigning a grade.
* **Date/Time API**: `BackupService` uses `java.time` to create timestamped backup folders.

### Advanced Concepts
* **Immutability**: The `CourseCode` class is an immutable value object.
* **Enums with Constructors**: The `Grade` enum has a constructor and a field to store grade points.
* **Custom Exceptions**: The project defines custom checked exceptions like `MaxCreditLimitExceededException` and `DuplicateEnrollmentException` for specific business rules.
* **Diamond Problem Resolution**: The `DataArchiver` class demonstrates how to resolve the diamond problem by explicitly overriding a default method from two different interfaces (`Searchable` and `Persistable`).

## How to Run

1.  **Prerequisites**: Ensure you have a Java Development Kit (JDK) installed (version 8 or later is recommended).
2.  **Compile**: From the project's root directory (`CCRM`), compile the source code:
    ```bash
    javac -d bin src/edu/ccrm/main/MainMenu.java
    ```
    This will compile `MainMenu.java` and all its dependencies, placing the `.class` files in the `bin` directory.
3.  **Run**: Execute the main class from the `bin` directory:
    ```bash
    java -cp bin edu.ccrm.main.MainMenu
    ```
4.  **Data Files**: The application expects `students.csv` and `courses.csv` files to be present in the `test-data` directory for the import functionality. Sample files are included in this project.

## Project Structure
