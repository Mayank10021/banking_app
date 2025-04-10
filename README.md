# banking_app
BankingApp is a simple web-based banking system built with JSP, Servlets, and MySQL, offering basic functionalities like account management, fund transfers, and transaction history.

# BankingApp

A simple Java-based Banking Application using JSP, Servlets, and MySQL. This project provides basic banking functionalities such as account creation, login, balance inquiry, fund transfers, and transaction history. It is built using Java EE technologies and follows the MVC architecture.

## Features

- User registration and login
- View account details
- Deposit and withdraw funds
- Transfer money between accounts
- View transaction history
- Admin functionalities (optional)

## Technologies Used

- Java 23
- JSP & Servlets
- Apache Tomcat 10
- MySQL
- JDBC
- HTML/CSS/Bootstrap (for frontend UI)
- JDBC MySQL Connector (`mysql-connector-java-8.0.17.jar`)

## Setup Instructions

### Prerequisites

- JDK 23 installed
- Apache Tomcat 10+
- MySQL Server
- MySQL Workbench (optional)
- Any Java IDE (e.g., IntelliJ IDEA, Eclipse)

### Database Setup

1. Create a database named `bankdb` (or update the DB name in the code if different).
2. Import the SQL file located in `/sql/` folder (if available) or manually create tables as required.
3. Update the DB credentials in the project (usually in `DBConnection.java` or similar utility class):

```java
String url = "jdbc:mysql://localhost:3306/bankdb";
String username = "root";
String password = "admin";
Running the Project
Import the project into your IDE as a Maven or Dynamic Web Project.

Place the JDBC driver JAR (mysql-connector-java-8.0.17.jar) in WEB-INF/lib.

Deploy the project to Apache Tomcat server.

Start the server and open the app in your browser:

arduino
Copy
Edit
http://localhost:8080/BankingApp/
Folder Structure
bash
Copy
Edit
BankingApp/
├── src/
│   └── com/bank/servlets/        # Servlet classes
│   └── com/bank/dao/             # DAO classes
│   └── com/bank/model/           # JavaBeans / Model classes
├── WebContent/
│   ├── WEB-INF/
│   │   └── web.xml               # Deployment descriptor
│   ├── css/                      # Stylesheets
│   ├── js/                       # JavaScript files
│   └── *.jsp                     # JSP pages
└── sql/                          # Database schema (if provided)
Screenshots
Add screenshots of login page, dashboard, and transaction screen here.
![image](https://github.com/user-attachments/assets/eec225a3-a889-4489-a356-59d632aac58a)
![image](https://github.com/user-attachments/assets/caa5671a-64cd-42b9-a125-a07cc3c87def)
![image](https://github.com/user-attachments/assets/698449da-b6c8-4931-a443-4bf8fdfba4f7)

Future Enhancements
Add email notifications for transactions

Password reset functionality

Admin dashboard

RESTful API support

License
This project is licensed under the MIT License - see the LICENSE file for details.

Author
Mayank Aneja
---

Would you like me
