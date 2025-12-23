# 📚 e-Shelf Library

**e-Shelf** is a web-based online library project that combines a responsive front-end interface with a PHP & MySQL backend.  
The application allows users to browse books through individual book pages, search and filter records from a database, and borrow books with live availability updates.

The project was developed as a semester assignment for the **Web Programming** course and serves as a practical introduction to full request–response web applications.

🔗 **Live demo:** https://e-shelf.page.gd

---

## ✨ Features

- Responsive online book library interface  
- Individual book pages for each title  
- Insert books into a MySQL database  
- Search and filter books by:
  - title
  - category
  - year
- Borrow books:
  - decrements available copies
  - logs borrow transactions in the database
- Live book availability fetched dynamically on page load
- Database credentials separated from source code for security

---

## 🛠 Tech Stack

### Frontend
- HTML  
- CSS  
- Bootstrap 4  

### Backend
- PHP 7.4+ (compatible with PHP 8.x)  
- MySQL / MariaDB  

### Development & Hosting
- Local development: XAMPP / MAMP / WAMP  
- Live hosting: InfinityFree  

---

## 📂 Project Structure

```text
e-shelf/
├── index.html
├── search_results.php
├── search_results.html
├── insert_book.html
├── insert_book.php
├── borrow.php
├── book_info.php
├── db.example.php
├── library_db.sql
├── style.css
├── images/
│   └── (book cover images)
├── Atomic Habits.html
├── Dune.html
├── Rich Dad Poor Dad.html
├── The Richest Man in Babylon.html
├── Χαμογέλα, ρε... τι σου ζητάνε.html
├── Χνότα στο τζάμι.html
├── Αναφορά Διαδικτυακός Προγραμματισμός Εργασία Εξαμήνου
├── LICENSE
├── .gitignore
└── .gitattributes
```
---

## 🚀 Getting Started (Local Setup)
### 1️⃣ Requirements
PHP 7.4 or newer

MySQL or MariaDB

Apache (via XAMPP / MAMP / WAMP)

### 2️⃣ Project Location
Copy the project folder into your local web root, for example:

text
Copy code
C:\xampp\htdocs\LibraryProjectprt2\
### 3️⃣ Start Services
Start Apache and MySQL from the XAMPP control panel.

### 4️⃣ Create the Database
Open phpMyAdmin

Go to Import

Select library_db.sql

Click Go

### 5️⃣ Configure Database Connection
The database configuration file is not tracked in the repository.

Copy:

text
Copy code
db.example.php → db.php
Edit db.php with your local credentials:

php
Copy code
$DB_HOST = 'localhost';
$DB_USER = 'root';
$DB_PASS = ''; // set a password if applicable
$DB_NAME = 'library_db';

### 6️⃣ Run the Project
Home page:
http://localhost/LibraryProjectprt2/index.html

Search & filter page (database-backed):
http://localhost/LibraryProjectprt2/search_results.php

---

## 💡 Tip:
search_results.php is the actual database-powered search page.
search_results.html is a static/demo version.

---

## 🔌 Backend Endpoints
search_results.php
Queries the database and displays filtered book results.

insert_book.php
Handles inserting new books into the database.

borrow.php
Handles the borrowing process:

decrements available copies

logs borrow entries

book_info.php
Returns JSON data containing live availability for a book.

All database-related files include the shared connection:

php
Copy code
require_once __DIR__ . '/db.php';

---

## 🎯 Project Purpose
Practice full web request–response workflows

Apply responsive front-end design principles

Work with PHP and MySQL for data persistence

Implement basic search, filtering, and state updates

Follow clean project structure and configuration separation

---

## 📄 License
This project is licensed under the MIT License and is intended for educational and portfolio use.
