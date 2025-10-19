# 🛒 E-Commerce Platform

This project is a simple yet functional **E-Commerce Website** designed for both **Customers** and **Admins**.  
It supports user registration, product browsing, cart management, and admin control features for efficient online shopping.

---

## 📘 Project Overview

This platform provides two main modules — one for **Users** and one for **Admins** — to handle shopping and management functionalities.

---

## 👤 1. User Section

This section explains how users interact with the website.

### 🧾 1.1 User Registration
Users can register on **`register.php`** by providing their **name**, **email**, and **password**.  
Once registered, they gain access to personalized features like the **shopping cart**.

### 🔑 1.2 Login and Logout
- **Login:** Users log in on **`login.php`** using their email and password.  
- **Logout:** The **`logout.php`** page securely ends their session.

### 🛍️ 1.3 Viewing Products
All products are displayed on the homepage (**`index.php`**) with:
- Product names  
- Prices  
- Descriptions  
- Images

### ➕ 1.4 Adding Products to Cart
Users can click **“Add to Cart”** on the homepage.  
Items are stored in the cart table for the logged-in user.

### 🛒 1.5 Managing Cart
The **`cart.php`** page allows users to:
- View their selected items  
- Update or remove items  
- View total price  

---

## 🧑‍💼 2. Admin Section

This section explains how admins manage the platform.

### 🔐 2.1 Admin Login and Logout
- **Login:** Admins log in at **`admin/login.php`**.  
- **Logout:** The **`admin/logout.php`** page securely ends the session.

### 🖥️ 2.2 Admin Dashboard
**`admin/dashboard.php`** provides a control panel where admins can:
- Add products  
- Edit products  
- Delete products  

### ➕ 2.3 Add Products
Admins use **`admin/add_product.php`** to add products with details like:
- Product name  
- Description  
- Price  
- Image upload  

### ⚙️ 2.4 Manage Products
The **`admin/manage_products.php`** page lists all products in a table with options to:
- **Edit** product details  
- **Delete** products  

---

## 🗄️ 3. Database Structure

### 👥 3.1 `users` Table
Stores all user (customer/admin) information:
- Username  
- Email  
- Hashed password  
- Role (`user` / `admin`)

### 📦 3.2 `products` Table
Stores product details such as:
- Name  
- Price  
- Description  
- Image filename  

### 🛍️ 3.3 `cart` Table
Tracks items added to users' carts:
- User ID  
- Product ID  
- Quantity  

---

## 🔁 4. Website Flow

### 🧩 4.1 User Registration
Validates input, hashes passwords, and saves user data to the database.

### 🔓 4.2 User Login
Verifies credentials and starts a session to grant personalized access.

### 🛒 4.3 Add to Cart
Saves the selected product details to the **cart table**, linked to the user’s ID.

### 📦 4.4 Admin Adds Product
Uploads product image and saves details in the **products table** for display.

### 🗑️ 4.5 Admin Deletes Product
Removes the product from the database and homepage view.

---

## 🔐 5. Security Measures

### 🧂 5.1 Password Security
Passwords are hashed using **`password_hash()`** before storing in the database.

### 🧩 5.2 Session Management
Sessions ensure access control:
- `$_SESSION['user_id']` for users  
- `$_SESSION['admin_id']` for admins  

### 🚫 5.3 Admin Access Control
The system checks the **role** field in the `users` table to restrict dashboard access to admins only.

---

## 📚 How to Use This Guide

Follow this README to understand:
- How users and admins interact with the platform  
- How data is stored and retrieved from the database  
- How the overall website flow works  

For detailed implementation, check the respective PHP files inside the project directories.

---

## 🧑‍💻 Author
**Santhosh Kumar N**  
📧 [santhoshkumar13012001@gmail.com](mailto:santhoshkumar13012001@gmail.com)  
🌐 [GitHub Profile](https://github.com/santhosh12133)

---
