# E-Commerce Web Application

A full-stack E-Commerce Web Application developed using **Flask**, **SQLite**, **HTML**, **CSS**, **Bootstrap**, and **JavaScript**. The application allows users to browse products, manage shopping carts, place orders, and track purchases through a secure and responsive platform.

## 📌 Project Overview

The E-Commerce Web Application is designed to simulate an online shopping platform where users can register, log in, browse products, add items to a shopping cart, and place orders. An admin panel is also included to manage products, users, and orders.

This project was developed as part of the **Thiranex Internship Program** to demonstrate full-stack web development, database management, authentication, and e-commerce system design.

---

## 🚀 Features

### 🔐 User Authentication

- User Registration
- User Login
- Secure Password Hashing using bcrypt
- Session Management
- Logout Functionality

### 🛍 Product Management

- View Products
- Product Categories
- Product Details
- Product Search
- Product Filtering

### 🛒 Shopping Cart

- Add Products to Cart
- Update Product Quantity
- Remove Products from Cart
- Calculate Total Price

### 📦 Order Management

- Place Orders
- View Order History
- Track Order Status

### 👨‍💼 Admin Dashboard

Admin can:

- Add Products
- Edit Products
- Delete Products
- Manage Orders
- View Registered Users

### 📱 Responsive Design

- Desktop Friendly
- Tablet Friendly
- Mobile Friendly

---

## 💻 Technologies Used

### Frontend

- HTML5
- CSS3
- Bootstrap 5
- JavaScript

### Backend

- Python
- Flask

### Database

- SQLite

### Security

- Flask-Bcrypt
- Session Management

### Development Tools

- VS Code
- Git
- GitHub

---

## 📂 Project Structure

```text
ecommerce-web-app/
│
├── app.py
├── ecommerce.db
├── requirements.txt
│
├── templates/
│   ├── login.html
│   ├── register.html
│   ├── home.html
│   ├── products.html
│   ├── cart.html
│   ├── checkout.html
│   ├── orders.html
│   └── admin.html
│
├── static/
│   ├── css/
│   │   └── style.css
│   │
│   ├── js/
│   │   └── script.js
│   │
│   └── images/
│
└── README.md
```

---

## 🗄 Database Schema

### Users Table

```sql
CREATE TABLE users(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    username TEXT NOT NULL,
    email TEXT UNIQUE NOT NULL,
    password TEXT NOT NULL
);
```

### Products Table

```sql
CREATE TABLE products(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name TEXT NOT NULL,
    description TEXT,
    price REAL NOT NULL,
    category TEXT,
    image TEXT,
    stock INTEGER
);
```

### Cart Table

```sql
CREATE TABLE cart(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    user_id INTEGER,
    product_id INTEGER,
    quantity INTEGER,
    FOREIGN KEY(user_id) REFERENCES users(id),
    FOREIGN KEY(product_id) REFERENCES products(id)
);
```

### Orders Table

```sql
CREATE TABLE orders(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    user_id INTEGER,
    total_amount REAL,
    order_date DATE,
    status TEXT,
    FOREIGN KEY(user_id) REFERENCES users(id)
);
```

---

## ⚙️ Installation Guide

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/ecommerce-web-app.git
cd ecommerce-web-app
```

### Step 2: Create Virtual Environment

```bash
python -m venv venv
```

### Step 3: Activate Virtual Environment

#### Windows

```bash
venv\Scripts\activate
```

#### Linux / macOS

```bash
source venv/bin/activate
```

### Step 4: Install Dependencies

```bash
pip install flask flask-bcrypt
```

### Step 5: Run the Application

```bash
python app.py
```

### Step 6: Open Browser

```text
http://127.0.0.1:5000
```

---

## 🛍 Application Workflow

### User Registration

Users create an account using:

- Username
- Email
- Password

Passwords are securely hashed before storage.

### User Login

Registered users can log in securely.

### Browse Products

Users can:

- View Products
- Search Products
- Filter Products

### Shopping Cart

Users can:

- Add Items
- Update Quantity
- Remove Items

### Checkout

Users provide:

- Shipping Address
- Contact Information
- Payment Method

### Place Order

Order details are stored in the database and assigned a status.

### Order Tracking

Users can track:

- Pending
- Processing
- Shipped
- Delivered

---

## 🔒 Security Features

### Password Hashing

Passwords are encrypted using bcrypt.

```python
bcrypt.generate_password_hash(password)
```

### SQL Injection Protection

Parameterized SQL queries are used.

```python
cursor.execute(
    "SELECT * FROM users WHERE email=?",
    (email,)
)
```

### Session Management

Authenticated sessions are maintained securely using Flask sessions.

---

## 📊 Admin Dashboard Features

### Product Management

- Add New Products
- Update Product Information
- Delete Products

### Order Management

- View Orders
- Update Order Status

### User Management

- View Registered Users

### Inventory Management

- Update Product Stock
- Monitor Product Availability

---

## 📸 Screenshots

### Home Page

- Featured Products
- Categories
- Navigation Menu

### Login Page

- Secure User Authentication

### Product Catalog

- Product Cards
- Search and Filter Options

### Shopping Cart

- Cart Summary
- Total Amount

### Checkout Page

- Shipping Information
- Order Confirmation

### Admin Dashboard

- Product Management
- Order Tracking

---

## 🎯 Learning Outcomes

This project demonstrates:

- Full Stack Web Development
- Flask Framework
- Database Design
- Authentication Systems
- CRUD Operations
- Shopping Cart Functionality
- Session Management
- E-Commerce Architecture
- Responsive Web Design
- Secure Coding Practices

---

## 🔮 Future Enhancements

- Online Payment Gateway Integration
- Product Reviews and Ratings
- Wishlist Feature
- Email Notifications
- Order Invoice Generation
- Product Recommendation System
- Multi-Vendor Marketplace
- Dark Mode

---

## 📈 Expected Outcome

A fully functional E-Commerce platform where users can browse products, manage shopping carts, place orders, and track purchases through a secure and responsive web application.

---

## 👨‍🎓 Internship Information

**Internship Program:** Thiranex Internship Program

**Domain:** Full Stack Web Development

**Project:** E-Commerce Web Application

---

## 👤 Author

**Dharani Prathipati**

Computer Science Engineering Student

GitHub: https://github.com/DharaniP-27

LinkedIn: Add Your LinkedIn Profile Link

---

## 📄 License

This project is developed for educational and internship purposes. Free to use and modify for learning and academic projects.# Thiranex-task-3
