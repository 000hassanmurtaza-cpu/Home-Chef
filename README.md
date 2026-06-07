# Home Chef - Database Management System (DBMS) Project

Home Chef is a complete database-driven web application connecting customers with talented home-based chefs. This system features order management, scheduling bookings, and active membership tracking. It is built as a complete Database Management System (DBMS) university / PBL project submission.

---

## 🌟 Key Features

### 👤 Customer Features
- **Secure Authentication**: Sign up and login with secure password hashing.
- **Browse Food Catalog**: Search list of gourmet dishes offered by various chefs.
- **Smart Food Ordering**: Add items to your cart, dynamically calculate checkout prices, and trace order processing history.
- **Private Chef Booking**: Hire chefs for customized dates, picking culinary specialities and experience levels.
- **Royal Club Membership**: Upgrade to premium tiers (Gold & Platinum) to enjoy delivery exemptions and price reductions.
- **Ratings & Reviews**: Give 1-5 star ratings and reviews to chefs.

### 👨‍🍳 Chef Features
- **Menu Management**: Add, update, and remove dishes from your menu.
- **Order Pipeline**: Control incoming orders (Accept, Prepare, Complete, Cancel).
- **Booking Manager**: Review scheduled client private event reservations and confirm/deny them.
- **Customer Reviews**: View reviews written specifically for you.

### 🔑 Admin Features
- **Global Logs Audit**: Monitor all user listings, memberships, and transaction logs.
- **General Order Logs**: Track and update status logs for orders in the system.

---

## 🛠️ Technology Stack
- **Frontend**: HTML5, Vanilla CSS3 (custom variables, dark mode glassmorphism panels, transitions), JavaScript (Vanilla ES6).
- **Backend**: PHP (Session handling, dynamic query loaders).
- **Database**: MySQL (relational keys, cascading deletes, indexes).

---

## 📁 Repository Structure

```text
github project/
│
├── database/
│   └── home_chef.sql        # Database initialization & mock data
│
├── css/
│   └── style.css            # Premium dark mode styling framework
│
├── js/
│   └── script.js            # Frontend calculations and alert controls
│
├── includes/
│   ├── config.php           # Database credential linkages and sanitizers
│   ├── header.php           # Dynamic navigation bar based on roles
│   └── footer.php           # Shared footer layouts
│
├── index.php                # Welcoming landing page
├── login.php                # Authentication page
├── register.php             # Conditional User/Chef registration fields
├── logout.php               # Session destruction handler
├── dashboard.php            # Analytics console adjusting to current role
├── dishes.php               # Catalog selector / Dish insertion console
├── order.php                # Customer checkout / Chef order lifecycle dashboard
├── booking.php              # Chef hiring scheduler
├── membership.php           # Royal Club Gold & Platinum payments simulation
├── review.php               # Feedback submission and review grid
└── README.md                # System documentation
```

---

## 🚀 Setup & Installation Instructions

### 1. Import Database SQL File
- Run your local database service (e.g., MySQL via XAMPP/WAMP or native installation).
- Open **phpMyAdmin** (`http://localhost/phpmyadmin`) or your preferred MySQL client (HeidiSQL, DBeaver, Command Line).
- Create a new database named `home_chef`:
  ```sql
  CREATE DATABASE home_chef;
  ```
- Import the database script `database/home_chef.sql` into the newly created database.

### 2. Configure Database Credentials
- Open `includes/config.php` and verify the database connection details:
  ```php
  define('DB_HOST', 'localhost');
  define('DB_USER', 'root');   // Replace with your database username
  define('DB_PASS', '');       // Replace with your database password
  define('DB_NAME', 'home_chef');
  ```

### 3. Running the Project

#### Option A: Running via PHP Built-in Server (Recommended)
1. Open your terminal/command prompt.
2. Navigate to the project folder (`github project/`).
3. Run the following command:
   ```bash
   php -S localhost:8000
   ```
4. Open your web browser and navigate to:
   ```text
   http://localhost:8000
   ```

#### Option B: Running via XAMPP
1. Move the folder `github project` to the `htdocs` directory:
   - Path on Windows: `C:\xampp\htdocs\github_project`
2. Start **Apache** and **MySQL** modules from the XAMPP Control Panel.
3. Access the application in your browser:
   ```text
   http://localhost/github_project/
   ```

---

## 🧪 Seeding & Test Accounts

You can test the different system roles using the seeded accounts:

| Role | Username / Email | Password |
|---|---|---|
| **Admin** | `admin@homechef.com` | `password123` |
| **Chef** | `gordon@homechef.com` | `password123` |
| **Customer** | `john@gmail.com` | `password123` |
