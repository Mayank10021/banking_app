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

```sql commands:-
CREATE DATABASE BankingDB;
use BankingDB;
CREATE TABLE accounts (
    account_id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(50) NOT NULL,
    balance DOUBLE DEFAULT 0.0,
    full_name VARCHAR(100),
    email VARCHAR(100)
);

CREATE TABLE transactions (
    transaction_id INT AUTO_INCREMENT PRIMARY KEY,
    account_id INT,
    transaction_type VARCHAR(10),
    amount DOUBLE,
    transaction_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    FOREIGN KEY (account_id) REFERENCES accounts(account_id)
);
select * from transactions;
SELECT * FROM transactions WHERE account_id = 1;
select * from transactions  where transaction_type is w and account_id=1;
SELECT transaction_type, amount, transaction_date 
FROM transactions 
WHERE account_id = 1 
ORDER BY transaction_date DESC;```
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
