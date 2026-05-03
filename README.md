[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/OFWe9D1G)
# 👗 Pastimes – Pre-Owned Branded Clothing Marketplace

> **Module:** Web Development Intermediate (WEDE6021)  
> **Student:** Nkuna Kuhlula  
> **Student Number:** ST10440743  
> **Institution:** Rosebank College (The Independent Institute of Education)  
> **Submission:** Part 2 – Prototype  
GROUP 14

---

## 📌 Project Overview

Pastimes is a fully functional PHP web application that allows users to buy and sell pre-owned branded clothing. The platform supports three user roles — **Buyer**, **Seller** and **Administrator** — each with their own set of features and access levels.
Use these credetentials to test the website 
Login credentials 
Role:Customer, Email: j.doe@abc.co.za Password:j.doe@abc.co.za
Role Customer, Email: Kuhlulankuna3@gmail.com Password: Mavutani11
Role: Admin, Email: admin@pastimes.co.za, Password: admin123
PasswordCustomerj.doe@abc.co.zapasswordAdminadmin@pastimes.co.zaadmin123
---

## 🗂️ Project Structure

```
ClothingStore/
│
├── DBConn.php                  # MySQLi database connection
├── createTable.php             # Drops & recreates tblUser, loads userData.txt
├── loadClothingStore.php       # Creates all 4 tables and seeds data
├── myClothingStore.sql         # Full DDL script with 30 entries
├── userData.txt                # 5 fictitious users (pipe-delimited)
│
├── login.php                   # Customer login with MD5 hash validation
├── register.php                # New user registration (pending approval)
├── index.php                   # Shop page – assoc array table display
├── addToCart.php               # AJAX cart handler
├── cart.php                    # View and manage cart
├── checkout.php                # Order confirmation, saves to tblAorder
├── logout.php                  # Destroys session
├── removeFromCart.php          # Removes item from session cart
│
├── css/
│   └── style.css               # Full professional stylesheet
│
├── images/
│   ├── item1.jpg               # Clothing image 1
│   ├── item2.jpg               # Clothing image 2
│   ├── item3.jpg               # Clothing image 3
│   ├── item4.jpg               # Clothing image 4
│   └── item5.jpg               # Clothing image 5
│
└── admin/
    ├── adminLogin.php          # Admin login with hash verification
    ├── dashboard.php           # Verify, add, edit, delete customers
    └── adminLogout.php         # Destroys admin session
```

---

## 🗄️ Database Tables

| Table | Description |
|-------|-------------|
| `tblUser` | All registered customers (buyers/sellers) |
| `tblAdmin` | Administrator accounts |
| `tblClothes` | Product listings |
| `tblAorder` | Customer orders |

---

## ⚙️ How to Run Locally

### Prerequisites
- [XAMPP](https://www.apachefriends.org/) (Apache + MySQL + PHP)
- [Visual Studio Code](https://code.visualstudio.com/)
- A modern web browser (Chrome or Firefox)

### Step 1 – Start XAMPP
1. Open **XAMPP Control Panel**
2. Click **Start** on **Apache**
3. Click **Start** on **MySQL**
4. Both must show green

### Step 2 – Place the project
Copy the `ClothingStore` folder to:
```
C:\xampp\htdocs\ClothingStore
```

### Step 3 – Set up the database
Open your browser and visit:
```
http://localhost/ClothingStore/loadClothingStore.php
```
This will automatically create all tables and load seed data.

### Step 4 – Open the app
```
http://localhost/ClothingStore/login.php
```

---

## 🔑 Login Credentials

### Customer Login
| Field | Value |
|-------|-------|
| Email | j.doe@abc.co.za |
| Password | password |

### Admin Login
| Field | Value |
|-------|-------|
| URL | http://localhost/ClothingStore/admin/adminLogin.php |
| Email | admin@pastimes.co.za |
| Password | admin123 |

---

## ✅ Features Implemented

### Database & Connection
- [x] ClothingStore database created with 4 tables
- [x] `userData.txt` with 5 fictitious entries
- [x] `DBConn.php` MySQLi connection file
- [x] `createTable.php` drops, recreates and loads tblUser
- [x] `loadClothingStore.php` builds full database
- [x] `myClothingStore.sql` DDL with 30 entries

### Login Page
- [x] Email and password login
- [x] Password compared against MD5 hash in tblUser
- [x] HTML5 validation on all fields
- [x] Sticky form on incorrect password
- [x] "User John Doe is logged in" display string
- [x] Pending users cannot log in until verified

### Registration
- [x] All fields required (HTML5 + server-side)
- [x] New accounts set to `pending` / `is_verified = 0`
- [x] Admin must verify before user can login

### Shop / Clothing Display
- [x] `tblClothes` read as associative array
- [x] Displayed in table with headers
- [x] Each row includes item image
- [x] AddToCart button with SellPrice popup
- [x] Returns to table after popup

### Admin Dashboard
- [x] Separate admin login with hashed password
- [x] Admin email address validated
- [x] Verify new customer registrations
- [x] Add new customers
- [x] Update existing customer details
- [x] Delete customers

---

## 🎨 Design & Code Standards

- **Font:** Poppins / Calibri
- **Colour Scheme:** Dark navy (`#1a1a2e`) + accent red (`#e94560`)
- **CSS Variables** used throughout for consistency
- **Responsive** layout using CSS Grid and Flexbox
- **Comments** on every PHP file explaining purpose and logic
- **Prepared statements** used for all database queries (SQL injection safe)
- **Naming convention:** camelCase for variables, descriptive function names

---

## 📹 Video Presentation

A video demonstration is included in the submission folder showing:
- Database setup and table creation
- New user registration with validation
- Login with correct and incorrect passwords (sticky form)
- "User is logged in" display
- Admin login and verification
- Add / Edit / Delete customers
- Shop page with assoc array display, images and cart popup

---

## 📚 References

- Depop (2024) *How does Depop work?* Available at: https://www.depop.com
- Vinted (2024) *How it works.* Available at: https://www.vinted.com
- PHP Documentation (2024) Available at: https://www.php.net/docs.php
- MySQLi Documentation (2024) Available at: https://www.php.net/manual/en/book.mysqli.php
- W3Schools PHP Tutorial (2024) Available at: https://www.w3schools.com/php

---

## 📄 Licence

This project was created for academic purposes at Rosebank College as part of the WEDE6021 module assessment.

© 2026 Nkuna Kuhlula – ST10440743
