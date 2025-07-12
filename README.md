# Airline-Database-Management-System
This is a mini airline management system that securely handles user information, personal details, payments, frequent flyer data, and travel passes. Inspired by Scandinavian Airlines, this system is designed to demonstrate secure data handling, normalization, and SQL integration via Python.

Features

- 👤 User registration and login with hashed passwords using **Argon2**
- 📄 Management of personal details, including passport photos
- 💳 Payment processing with date and amount tracking
- 🛫 Frequent flyer point tracking and membership management
- 🎟️ Travel pass issuance and expiry management
- 🔐 Secure SSH tunneling to connect with a remote MySQL database
- ✅ CRUD operations (Create, Read, Update, Delete) with data validation
- 🔍 Test cases implemented to verify system logic and error handling

  
Tech Stack

- **Python 3**
- **MySQL**
- **SSH Tunneling** with `sshtunnel`
- **Password Hashing** with `passlib` (Argon2)
- **CSV Data Import** with `pandas` and `csv`
- **ERD** in Crow’s Foot Notation
- **3NF Database Design**

  
Database Description
  | Table | Description |
|-------|-------------|
| `Users` | Stores user login credentials (username, hashed password, email) |
| `PersonalDetails` | Stores name, address, phone number, DOB, and passport photo |
| `Payments` | Stores payment type, date, and amount |
| `FrequentFlyer` | Stores loyalty program name, points, and membership level |
| `TravelPass` | Stores pass type and expiry details linked to frequent flyer |

All foreign keys use `ON DELETE CASCADE` to maintain referential integrity.


Password Security

Passwords are hashed using the **Argon2** algorithm before being stored. This ensures:
- Strong resistance to brute-force attacks
- Salted and non-reversible storage
- Industry-level security

- python
from passlib.hash import argon2
hashed_password = argon2.hash(password)

Normalization and Design Quality
1.Database is normalized up to 3NF

2.No partial or transitive dependencies

3.No multivalued dependencies

4.Minimal redundancy and high scalability

Why via python?
-In real-world applications, different parts are often built using different languages like Python, Java, or C , and they usually connect to a database like SQL for storing data.

By using Python in this project, I learned how programming languages interact with a database, handle data securely, and automate tasks like data validation and updates.

It gave me a better understanding of how backend systems work in real applications and helped me automate the workflow, add security like password hashing, and handle files and errors more smoothly. It made the project more practical and realistic.
