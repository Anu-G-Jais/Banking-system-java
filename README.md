# 💰 Banking App

Welcome to the Banking App, a simple yet powerful Java application for managing your finances! 🚀

## 📋 Table of Contents

- [Features](#features)
- [Setup](#setup)
  - [Database Setup](#database-setup)
  - [Java Setup](#java-setup)
- [Usage](#usage)
  - [Main Menu](#main-menu)
  - [User Registration](#user-registration)
  - [User Login](#user-login)
  - [Account Operations](#account-operations)
- [Contributing](#contributing)
- [License](#license)

## ✨ Features

- User registration and login system 📝
- Account creation with a unique account number 🔢
- Money transfer between accounts 💸
- Balance checking ⚖️
- User-friendly command-line interface 🖥️

## 🛠️ Setup

### Database Setup

1. Install MySQL on your machine if not already installed.
2. Create a new database named `BankDB`.
3. Execute the SQL script in `database.sql` to create the necessary tables (`User` and `Accounts`).

 -- Step 1: Create the BankDB database
CREATE DATABASE IF NOT EXISTS BankDB;

-- Step 2: Use the BankDB database
USE BankDB;

-- Step 3: Create the "account" table with modified column name
CREATE TABLE IF NOT EXISTS account (
    account_number BIGINT NOT NULL PRIMARY KEY AUTO_INCREMENT,
    full_name VARCHAR(200) NOT NULL,
    email VARCHAR(200) NOT NULL UNIQUE,
    balance DECIMAL(10,2),
    security_pin CHAR(4)
);

-- Step 4: Create the "user" table
CREATE TABLE IF NOT EXISTS user (
    full_name VARCHAR(200),
    email VARCHAR(200) PRIMARY KEY,
    password VARCHAR(200)
);


### Java Setup

1. Clone this repository to your local machine.
2. Open the project in your favorite Java IDE (e.g., IntelliJ IDEA, Eclipse).
3. Ensure you have the MySQL Connector/J library in your classpath.
4. Update the `url`, `username`, and `password` variables in `BankingApp.java` to match your MySQL configuration.

## 🚀 Usage

### Main Menu

Upon running the application, you will be presented with the main menu:

1. **Register:** Allows a new user to register.
2. **Login:** Enables existing users to log in.
3. **Exit:** Closes the application.

### User Registration

If you choose to register, you will be prompted to enter your full name, email, and password. Ensure that the email is unique, as each user is identified by their email.

### User Login

Existing users can log in by providing their email and password. If the provided credentials are correct, you will be logged in.

### Account Operations

Once logged in, the application allows you to perform various account operations:

1. **Open a new Bank Account:** Creates a new bank account associated with the logged-in user.
2. **Debit Money:** Withdraws money from the account.
3. **Credit Money:** Deposits money into the account.
4. **Transfer Money:** Transfers money between two accounts.
5. **Check Balance:** Displays the current balance of the logged-in user.

## 🤝 Contributing

Feel free to contribute to the development of this banking app by submitting issues or pull requests. Contributions are welcome and appreciated!
