# Advanced-Ticket-Booking-System# 🎟️ Advanced Ticket Booking System

## 📌 Project Overview

The **Advanced Ticket Booking System** is an SQL-based mini project developed for the subject **Advanced Database Management System (ADBMS)**.
This project simulates a real-world ticket booking platform used in movie theaters, railway reservations, bus ticketing systems, and event management applications.

The main objective of this project is to demonstrate how databases handle:

* Multiple users booking seats simultaneously
* Transaction management
* Concurrency control
* Deadlock prevention
* Locking mechanisms
* Rollback handling
* Optimistic locking
* Waiting queue management

---

# 🚀 Features

✅ User & Show Management
✅ Seat Reservation System
✅ Transaction Handling using `COMMIT` & `ROLLBACK`
✅ Concurrency Control using `FOR UPDATE`
✅ Parallel Booking with `SKIP LOCKED`
✅ Optimistic Locking using Version Control
✅ Deadlock Detection & Prevention
✅ Payment Failure Rollback Handling
✅ Isolation Level Analysis
✅ Auto Release of Expired Seat Locks
✅ Waiting Queue System for Fully Booked Shows

---

# 🛠️ Technologies Used

| Technology         | Purpose                |
| ------------------ | ---------------------- |
| SQL                | Database Queries       |
| MySQL / PostgreSQL | Database Management    |
| Stored Procedures  | Booking Logic          |
| Transactions       | Data Consistency       |
| Locking Mechanisms | Prevent Double Booking |

---

# 📂 Database Tables

## 1. Users

Stores registered user information.

| Column   | Description    |
| -------- | -------------- |
| user_id  | Unique User ID |
| username | User Name      |
| email    | User Email     |

---

## 2. Shows

Stores movie/event details.

| Column      | Description     |
| ----------- | --------------- |
| show_id     | Unique Show ID  |
| title       | Show/Movie Name |
| show_time   | Timing          |
| total_seats | Total Seats     |

---

## 3. Seats

Stores seat information and booking status.

| Column      | Description                 |
| ----------- | --------------------------- |
| seat_id     | Unique Seat ID              |
| show_id     | Related Show                |
| seat_number | Seat Label                  |
| status      | AVAILABLE / BOOKED          |
| version     | Used for Optimistic Locking |

---

## 4. Bookings

Stores successful booking records.

| Column     | Description    |
| ---------- | -------------- |
| booking_id | Booking ID     |
| user_id    | User Reference |
| seat_id    | Seat Reference |
| status     | Booking Status |

---

# 📚 Concepts Implemented

* ACID Properties
* Transactions
* Concurrency Control
* Pessimistic Locking
* Optimistic Locking
* Deadlocks
* Isolation Levels
* Rollback & Commit
* Event Scheduler
* Foreign Keys & Constraints

---

# 🔥 Advanced Features

## 🔒 Concurrency Control

Used `FOR UPDATE NOWAIT` to prevent two users from booking the same seat simultaneously.

## ⚡ Parallel Booking

Implemented `FOR UPDATE SKIP LOCKED` for faster parallel seat booking.

## 🧠 Optimistic Locking

Used a `version` column to detect concurrent updates without locking rows.

## ♻️ Rollback Handling

If payment fails during booking, the transaction automatically rolls back and releases the seat.

## ⏳ Auto Release System

Locked seats are automatically released after timeout using MySQL Event Scheduler.

## 📌 Waiting Queue

Users are added to a waiting queue if all seats are booked.

---

# ▶️ How to Run the Project

## Step 1: Create Database

```sql
CREATE DATABASE ticket_booking_db;
```

## Step 2: Use Database

```sql
USE ticket_booking_db;
```

## Step 3: Run SQL File

Execute the schema and seed data SQL script.

## Step 4: Test Queries

Run booking transactions and concurrency handling queries.

---

# 📈 Learning Outcomes

Through this project, I learned:

* Advanced SQL Query Writing
* Database Design
* Transactions & Locking
* Real-Time Concurrency Handling
* Stored Procedures
* Deadlock Prevention
* Rollback Management
* Event Scheduling in MySQL

---

# 💡 Real-World Applications

* 🎬 Movie Ticket Booking Systems
* 🚆 Railway Reservation Systems
* 🚌 Bus Booking Platforms
* 🎤 Concert/Event Ticketing Systems

---

# 👨‍💻 Author

MCA Mini Project
Advanced Database Management System (ADBMS)
