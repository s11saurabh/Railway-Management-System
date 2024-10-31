# Railway-Management-System


A comprehensive Railway Management System developed as a course project for a Database Management Systems (DBMS) subject. This project is designed to streamline operations for railway staff and enable users to book, manage, and cancel tickets efficiently. The system leverages a MySQL database to handle complex scheduling, seat allocation, and high transaction volumes while maintaining data integrity.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [System Architecture](#system-architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Database Schema](#database-schema)
- [Future Improvements](#future-improvements)
- [License](#license)

## Overview
The Railway Management System provides an end-to-end solution for railway operations and ticket booking. By using a robust SQL database, secure user authentication, and a responsive user interface, this system enables users to interact with a dynamic platform to manage bookings. The project includes a back-end setup using Node.js and Express with MySQL, and a front-end interface built with HTML, CSS, and React.

## Features
### User Features
- **Sign Up and Login**: Users can register and sign in to book tickets.
- **Real-time Booking and Cancellation**: Book, cancel, and manage tickets in real-time.
- **Seat Allocation**: Dynamic seat allocation based on real-time availability.
- **Ticket Management**: Users can view their booking history and manage current reservations.
  
### Admin/Staff Features
- **Schedule Management**: Staff can create and manage train schedules, ensuring seamless operation.
- **Ticketing and Booking System**: Admins can access ticketing data and assist in bookings.
- **User Management**: Manage user data securely and access booking records for maintenance and troubleshooting.

## Tech Stack
### Frontend
- **HTML** & **CSS**: Basic structure and styling of the static web pages.
- **React**: Dynamic user interface with real-time updates and seamless navigation.

### Backend
- **Node.js** & **Express**: Server-side functionality, API endpoints for handling requests.
- **PHP**: For database operations and connecting the MySQL database on XAMPP.

### Database
- **MySQL**: Relational database management for handling user data, booking records, schedules, and transactions.
- **mysql2**: A MySQL client for Node.js, used to streamline MySQL interactions.

### Authentication
- **Passport.js**: Secure user authentication and session management for both users and staff.

### Server Environment
- **XAMPP**: Local development environment to set up and run MySQL, PHP, and Apache server locally.

## System Architecture
The system is structured around a client-server model with a clear separation of concerns:
- **Frontend (Client)**: The React-based front end interacts with the backend server via HTTP requests. The frontend manages user interactions and displays real-time booking updates.
- **Backend (Server)**: Built with Node.js and Express, the server handles all client requests, processes data, and communicates with the MySQL database.
- **Database (MySQL)**: A relational structure that manages tables for users, tickets, schedules, and seat allocations.

## Installation
To install and run the Railway Management System on your machine, follow these steps:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/s11saurabh/railway-management-system.git
   cd railway-management-system
   ```

2. **Database Setup**:
   - Sign up or log in to your MySQL database.
   - Run the `railway.sql` script to set up the necessary tables and data.
   - Save the database, and update the `db.php` file with your MySQL username and password.

3. **Configure Local Environment**:
   - If using XAMPP, place the project files in the `htdocs` folder inside the XAMPP directory:
     ```
     ~\xampp\htdocs\railway
     ```
   - Ensure that the MySQL service is running in the XAMPP control panel.

4. **Install Node.js dependencies**:
   ```bash
   npm install
   ```

5. **Run the Application**:
   - Start the server:
     ```bash
     node app.js
     ```
   - Open `index.html` in your browser, or navigate to `http://localhost/railway` if using XAMPP.

## Usage
1. **User Signup and Login**:
   - Navigate to the login page, create an account, and sign in to access the booking system.
   
2. **Booking Tickets**:
   - Select a train, check seat availability, and proceed to book your ticket.
   
3. **Admin Access**:
   - Admins can log in to manage schedules, view booking data, and assist users.

4. **Seat Management**:
   - The system dynamically updates seat availability, enabling real-time bookings and cancellations.

## Project Structure

```plaintext
.
├── config/
│   ├── db.php                 # Database configuration file
├── data/
│   ├── railway.sql            # SQL script for setting up the database
├── public/
│   ├── css/                   # CSS stylesheets
│   ├── js/                    # JavaScript files
│   └── index.html             # Landing page
├── server/
│   ├── app.js                 # Express server file
│   ├── routes/                # Route files for different API endpoints
├── views/
│   ├── booking.html           # Booking page
│   ├── login.html             # Login page
│   ├── signup.html            # Signup page
└── README.md
```

## Database Schema
The MySQL database schema is structured as follows:

- **Users Table**: Stores user data (ID, name, email, password).
- **Trains Table**: Stores train schedules, train numbers, destinations, and timings.
- **Bookings Table**: Records booking details, user ID, train ID, and seat information.
- **Seats Table**: Manages seat availability for each train.

Refer to `railway.sql` for detailed table structures and relationships.

## Future Improvements
- **Payment Integration**: Add a secure payment gateway for online payments.
- **Enhanced Security**: Implement additional security measures like OTP verification and 2FA.
- **Notifications**: Email or SMS alerts for booking confirmation and schedule updates.
- **Analytics**: Insights for admin users on booking trends, peak travel times, and user preferences.

## License
This project is open-source and available under the APACHE License. See the [LICENSE](LICENSE) file for details.
