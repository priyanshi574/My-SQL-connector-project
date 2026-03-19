# 🔐 Login & Registration App (Python + MySQL + Tkinter)

A simple desktop-based Login and Registration system built using **Python**, **Tkinter**, and **MySQL**. This application allows users to register, store their details in a database, and log in securely.

---

## 🚀 Features

* User Registration with:

  * Name
  * Email (unique)
  * Age
  * Sex
  * Password (with confirmation)
* Login Authentication
* Password visibility toggle 👁️
* Input validation
* MySQL database integration
* Simple GUI using Tkinter

---

## 🛠️ Technologies Used

* Python
* Tkinter (GUI)
* MySQL
* mysql-connector-python

---

## 📦 Installation

### 1. Clone the repository

```bash
git clone https://github.com/your-username/login-app.git
cd login-app
```

### 2. Install dependencies

```bash
pip install mysql-connector-python
```

### 3. Setup MySQL

* Make sure MySQL server is running
* Update your credentials in the code if needed:

```python
host="localhost"
user="root"
password="1234"
```

### 4. Create Database

Run this snippet once:

```python
import mysql.connector

db = mysql.connector.connect(
    host="localhost",
    user="root",
    password="1234"
)

cursor = db.cursor()
cursor.execute("CREATE DATABASE IF NOT EXISTS login_app")
```

---

## 🗄️ Database Schema

```sql
CREATE TABLE IF NOT EXISTS users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    age INT,
    sex VARCHAR(10),
    password VARCHAR(255)
);
```

---

## ▶️ How to Run

```bash
python your_script_name.py
```

---

## 📸 Screens

* Registration Window
* Login Window
* Success Window

---

## ⚠️ Important Notes

* Passwords are currently stored in plain text (not secure)
* For production use, implement password hashing using `bcrypt`

---

## 🔒 Future Improvements

* Add password hashing (bcrypt)
* Email validation with regex
* Forgot password feature
* Dashboard after login
* Better UI design

---

## 🤝 Contributing

Feel free to fork this repository and improve it!

---

## 📄 License

This project is open-source and free to use.

---

## 💡 Author

PRIYANSHI
GitHub: https://github.com/priyanshi574
