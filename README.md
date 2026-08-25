# 📘 ELHA - Personalized Beauty & Fashion E-Commerce Platform

## README for GitHub Submission

---

# ELHA - E-Commerce Platform

> **Personalized Beauty & Fashion E-Commerce Platform**  
> A complete web application built with PHP, MySQL, and Bootstrap 5.

---

## 📌 Project Overview

**ELHA** is a fully functional e-commerce platform designed for beauty and fashion products. The platform allows customers to browse products, add items to cart, place orders with Cash on Delivery, manage their profile, and track orders. It also includes a complete admin panel for managing products, categories, orders, customers, and recommendations.

---

## 🚀 Features

### 👤 Customer Panel

| Feature | Description |
|---------|-------------|
| **User Registration** | Register with name, email, phone, and password |
| **User Login/Logout** | Secure login using email and password with session management |
| **Profile Management** | Update name, email, phone, and change password |
| **Product Browsing** | View all products with category, price, and discount information |
| **Search & Filter** | Search products by name, filter by category and price range |
| **Product Details** | View product images, description, price, stock, and add to cart |
| **Shopping Cart** | Add/remove products, update quantities, and view subtotal |
| **Wishlist** | Save favorite products for later purchase |
| **Checkout (COD)** | Place orders with Cash on Delivery, mandatory delivery address |
| **Order History** | View all past orders with order number, date, total, and status |
| **Order Tracking** | Track order status with visual timeline |
| **Complete the Look** | View matching products suggested for a selected product |
| **Gift Finder** | Find products based on occasion, recipient, and budget |
| **Personalised Recommendations** | Select skin type and concern to get recommended products |
| **Deal of the Week** | View weekly discounted products on homepage |

### 🔐 Admin Panel

| Feature | Description |
|---------|-------------|
| **Admin Login** | Secure admin login with email and password |
| **Dashboard** | View total products, customers, orders, pending orders, matches, and recommendation rules |
| **Product Management** | Add, edit, delete, and view products with image upload |
| **Category Management** | Add, edit, and delete product categories |
| **Order Management** | View all orders, update order status |
| **Customer Management** | View all registered customers and toggle active/inactive status |
| **Complete the Look Management** | Create and delete product matching relationships |
| **Recommendation Rules Management** | Create rules for customer recommendations |

---

## 🛠️ Technologies Used

| Category | Technology |
|----------|------------|
| **Frontend** | HTML5, CSS3, JavaScript, Bootstrap 5 |
| **Backend** | PHP (Plain PHP - No Framework) |
| **Database** | MySQL |
| **Local Server** | XAMPP (Apache + MySQL) |
| **Authentication** | PHP Sessions |
| **Security** | Password Hashing, Prepared Statements, Session Management |

---

## 📁 Project Structure

```
elha/
├── admin/                     # Admin Panel
│   ├── index.php             # Dashboard
│   ├── products.php          # Product Management
│   ├── product-add.php       # Add Product
│   ├── product-edit.php      # Edit Product
│   ├── categories.php        # Category Management
│   ├── orders.php            # Order Management
│   ├── order-details.php     # Order Details
│   ├── customers.php         # Customer Management
│   ├── complete-look.php     # Complete the Look Management
│   ├── recommendation-rules.php # Recommendation Rules
│   ├── login.php             # Admin Login
│   ├── logout.php            # Admin Logout
│   └── includes/             # Admin Reusables
├── assets/
│   ├── css/style.css         # Custom Styles
│   ├── js/script.js          # Custom JavaScript
│   └── images/               # Product Images
├── config/
│   ├── config.php            # Site Configuration
│   └── database.php          # Database Connection
├── includes/
│   ├── header.php            # HTML Head
│   ├── navbar.php            # Navigation Bar
│   ├── footer.php            # Footer
│   ├── functions.php         # Helper Functions
│   └── auth.php              # Authentication Functions
├── ajax/                     # AJAX Handlers
├── index.php                 # Homepage
├── shop.php                  # Product Listing
├── product.php               # Product Details
├── cart.php                  # Shopping Cart
├── wishlist.php              # Wishlist
├── checkout.php              # Checkout (COD)
├── orders.php                # Order History
├── order-details.php         # Order Details
├── tracking.php              # Order Tracking
├── profile.php               # User Profile
├── login.php                 # Customer Login
├── register.php              # Customer Registration
├── logout.php                # Customer Logout
├── recommendations.php       # Product Recommendations
├── complete-look.php         # Complete the Look
├── gift-finder.php           # Gift Finder
└── database/
    └── elha_ecommerce.sql    # Complete Database Dump
```

---

## 💾 Database Schema

The database includes the following tables:

| Table | Purpose |
|-------|---------|
| `users` | Customer accounts |
| `admins` | Admin accounts |
| `categories` | Product categories |
| `products` | Product details with price, stock, images |
| `wishlist` | Customer wishlist items |
| `cart` | Customer shopping cart |
| `orders` | Order header details |
| `order_items` | Individual products in each order |
| `product_matches` | Complete the Look matching relationships |
| `recommendation_rules` | Rules for product recommendations |
| `recommendation_products` | Products linked to recommendation rules |
| `weekly_deals` | Weekly discounted products |

---

## ⚙️ Installation & Setup

### Prerequisites

- XAMPP (Apache + MySQL)
- PHP 7.4 or higher
- MySQL 5.7 or higher

### Step 1: Clone or Download

```bash
git clone https://github.com/yourusername/elha.git
```

Or download and extract the ZIP file.

### Step 2: Move to htdocs

Move the project folder to your XAMPP `htdocs` directory:

```
C:\xampp\htdocs\elha\
```

### Step 3: Import Database

1. Open phpMyAdmin: `http://localhost/phpmyadmin`
2. Create a new database named `elha_ecommerce`
3. Import the SQL file: `database/elha_ecommerce.sql`

### Step 4: Configure

Open `config/config.php` and update the BASE_URL:

```php
define('BASE_URL', 'http://localhost/elha');
```

### Step 5: Start XAMPP

1. Start Apache
2. Start MySQL

### Step 6: Access the Website

- **Customer Website:** `http://localhost/elha/`
- **Admin Panel:** `http://localhost/elha/admin/`

---

## 🔑 Login Credentials

### Admin Login

| Field | Value |
|-------|-------|
| **Email** | `elha@gmail.com` |
| **Password** | `elha123` |

### Customer Login

Register a new account from the website.

---

## 📊 Business Logic

| Feature | Logic |
|---------|-------|
| **Delivery Charge** | Inside Dhaka: ৳80, Outside Dhaka: ৳150, Free above ৳1000 |
| **Order Status Flow** | Pending → Confirmed → Processing → Shipped → Delivered (or Cancelled) |
| **Product Stock** | Automatically reduces when order is placed |
| **Payment Method** | Cash on Delivery (COD) only |
| **Recommendations** | Admin creates rules → Customer selects skin type + concern → Matching products displayed |

---

## 🔒 Security Features

| Security Measure | Implementation |
|------------------|----------------|
| Password Hashing | `password_hash()` and `password_verify()` |
| SQL Injection Prevention | PDO Prepared Statements |
| Session Authentication | PHP sessions |
| Input Validation | Server-side validation |
| Output Escaping | `htmlspecialchars()` to prevent XSS |
| Admin Authentication | Separate session for admin panel |

---

## 📸 Screenshots

### Homepage
![Homepage](screenshots/homepage.png)

### Product Listing
![Shop](screenshots/shop.png)

### Shopping Cart
![Cart](screenshots/cart.png)

### Checkout
![Checkout](screenshots/checkout.png)

### Admin Dashboard
![Admin Dashboard](screenshots/admin-dashboard.png)

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is for educational purposes only.

---

## 👨‍💻 Author

**[Your Name]**  
[Your University]  
[Your Email]  

---

## 🙏 Acknowledgements

- W3Schools for PHP, MySQL, and Bootstrap tutorials
- Bootstrap Team for the amazing framework
- PHP.net for PHP documentation
- Apache Friends for XAMPP

---

## 📚 References

1. W3Schools. (2026). *PHP Tutorial*. W3Schools.com.
2. W3Schools. (2026). *Bootstrap 5 Tutorial*. W3Schools.com.
3. W3Schools. (2026). *MySQL Tutorial*. W3Schools.com.
4. PHP Group. (2026). *PHP Manual*. php.net.
5. Bootstrap Team. (2026). *Bootstrap Icons*. getbootstrap.com.

---

## 📞 Contact

For any questions or support, please contact:
- **Email:** [your-email@example.com]
- **GitHub:** [your-github-username]

---

**⭐ Star this repository if you found it helpful!**

---

## 🎯 Quick Links

| Link | URL |
|------|-----|
| **Customer Homepage** | `http://localhost/elha/` |
| **Admin Panel** | `http://localhost/elha/admin/` |
| **phpMyAdmin** | `http://localhost/phpmyadmin` |

