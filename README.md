# Cell Phone Company Dashboard

This project is a web application for managing customer data, phone plans, payments, and call records for a cell phone company. It includes features such as user registration, login, customer and employee dashboards, and secure access control using JWT authentication.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [License](#license)

## Project Overview

The Cell Phone Company Dashboard is a full-stack web application that provides an interface for managing phone plans, viewing transaction and payment history, and accessing call records. The app is designed with role-based access for customers and employees, offering each group a tailored dashboard to view relevant information.

## Features

- **User Authentication**: Secure login and registration with password hashing and JSON Web Tokens (JWT) for authentication.
- **Role-Based Access Control**: Separate views and permissions for customers and employees.
- **Customer Dashboard**: Provides an overview of linked phone plans, recent call and data usage, payment history, and balance.
- **Employee Management**: Includes employee access to manage customer records, generate reports, and view statistics.
- **Payment System**: Allows customers to make payments and updates balances.
- **Error Handling**: Includes error handling and user feedback for smooth operation.

## Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Node.js, Express
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens) with bcrypt for password hashing

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) and npm installed
- [PostgreSQL](https://www.postgresql.org/) installed and configured

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/cell-phone-dashboard.git
    cd cell-phone-dashboard
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Set up the environment variables:

   Create a `.env` file in the root directory and configure the following variables:

    ```plaintext
    USER=<your_postgres_user>
    HOST=localhost
    DATABASE=<your_database_name>
    PASSWORD=<your_postgres_password>
    PORT=5432
    JWT_SECRET=<your_jwt_secret>
    ```

4. Set up the database:

   Use the included DDL files or run SQL commands to set up the necessary tables (such as `users`, `customer`, `phoneplan`, `bankaccount`, etc.) in your PostgreSQL database.

5. Start the server:

    ```bash
    node server.js
    ```

6. Access the app in your browser at `http://localhost:3000`.

## Usage

1. **Register a New User**: 
   - Use the registration page to create a new user (either customer or employee).
2. **Login**:
   - Access the login page to authenticate with your registered credentials.
3. **Dashboard**:
   - After logging in, customers and employees are redirected to their respective dashboards where they can view information and manage their accounts.
4. **Payments**:
   - Customers can initiate a payment from the dashboard, which updates their balance and logs the transaction.

## Project Structure

```plaintext
├── public
│   ├── index.html          # Main HTML page
│   ├── login.html          # Login page
│   ├── register.html       # Registration page
│   ├── dashboard.html      # Dashboard content
│   ├── styles.css          # Main CSS file
│   ├── loginstyles.css     # Login page CSS
│   └── app.js              # Frontend JavaScript for API interactions
├── server.js               # Main backend server file
├── .env                    # Environment variables
└── README.md               # Project documentation
