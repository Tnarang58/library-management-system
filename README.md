# Library Management System

A Library Management System built using Java Spring Boot for managing books, users, and transactions such as book issuance, returns, and fines. The system includes an admin panel for managing the library, and a user panel for accessing and interacting with library resources.

## Features

### Admin Features:
- **Maintenance Module**: Manage books, users, and transactions.
- **Reports Module**: Generate reports on issued books, returned books, and fines.
- **Transactions Module**: Issue and return books with automatic fine calculation.

### User Features:
- **View Reports**: Users can view reports about the books they’ve issued and returned.
- **Issue Books**: Search for available books and issue them.
- **Return Books**: Return issued books and view fines if any.
- **Membership Management**: Add or update membership with different durations (6 months, 1 year, 2 years).

### Core Functionalities:
- **Book Availability Check**: Radio buttons to select books, with validation to ensure a book is selected before issuing.
- **Issue Date Validation**: Issue dates cannot be earlier than today, and return dates are automatically set.
- **Fine Calculation**: If a book is returned late, the system will calculate a fine based on the due date.
- **User & Admin Roles**: Admin can access all modules, while regular users have limited access.

## Project Structure

```
library-management-system/
├── src/
│   ├── main/
│   │   ├── java/com/tanishq/librarymanagementsystem/
│   │   │   ├── controller/
│   │   │   ├── model/
│   │   │   ├── repository/
│   │   │   ├── service/
│   │   │   └── LmsApplication.java
│   │   └── resources/
│   │       ├── templates/  # Thymeleaf templates (HTML views)
│   │       ├── static/     # Static resources (CSS, JS, images)
│   │       └── application.properties
│   └── test/  # Test files
├── pom.xml    # Maven dependencies
└── README.md  # Project documentation
```

## Technologies Used

- **Java 11**
- **Spring Boot**
- **Thymeleaf** for front-end
- **MySQL** for the database
- **Maven** for dependency management
- **Git** for version control

## Installation & Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/Tnarang58/library-management-system.git
   cd library-management-system
   ```

2. Install dependencies using Maven:
   ```bash
   mvn clean install
   ```

3. Configure your MySQL database in `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/library_management_system
   spring.datasource.username=root
   spring.datasource.password=yourpassword
   spring.jpa.hibernate.ddl-auto=update
   ```

4. Run the application:
   ```bash
   mvn spring-boot:run
   ```

5. Open your browser and navigate to:
   ```
   http://localhost:8080
   ```

## License

This project is licensed under the MIT License.
