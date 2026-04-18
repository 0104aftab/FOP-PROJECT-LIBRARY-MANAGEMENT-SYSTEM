# 📚 Library Management System (C Project)

A file-based **Library Management System** built in C that allows administrators and users to manage books, issue/return records, and student accounts using persistent storage.

---

## 🚀 Features

### 👨‍💼 Admin Functionalities

* Add new books
* Display all books
* Search books by title
* Issue books to students
* Return books and calculate fines
* Count total books in library

### 👨‍🎓 User Functionalities

* Sign up and login using PRN & password
* View available books
* Search books

### 📂 File-Based Storage

* Books stored in CSV format
* Students stored in text file
* Issued books tracked with issue/return details

---

## 📁 Project Structure

```
├── LMS_Final.c.txt        # Main C source code :contentReference[oaicite:0]{index=0}
├── books.csv.txt         # Book database :contentReference[oaicite:1]{index=1}
├── Students.txt          # Student records :contentReference[oaicite:2]{index=2}
├── Issued_Books.txt      # Issued book records :contentReference[oaicite:3]{index=3}
```

---

## 🧠 How It Works

### 📚 Books Management

* Books are stored with fields:

  * ID, Title, Author, Genre, Year
  * Total Copies, Available Copies 
* Admin can add new books dynamically
* Availability updates automatically on issue/return

### 👤 Student Management

* Students register using:

  * PRN (unique ID)
  * Name
  * Password 
* Authentication is required for access

### 🔄 Issue & Return System

* Books can be issued for **14 days**
* Due date is auto-calculated
* Fine = ₹1 per day after due date
* Records stored with:

  * Issue date, Due date, Return date
  * Return status and fine 

---

## ⚙️ Setup Instructions

### 1. Update File Paths

In the code, update file paths if needed:

```c
#define FILE_1 "books.csv.txt"
#define FILE_2 "Students.txt"
#define FILE_3 "Issued_Books.txt"
```

(Currently hardcoded for Windows paths.)

---

### 2. Compile the Program

```bash
gcc LMS_Final.c.txt -o lms
```

---

### 3. Run the Program

```bash
./lms
```

---

## 🔐 Default Admin Credentials

```
Username: FOP
Password: MitWpu123
```

---

## 🖥️ Menu Flow

### Main Menu

```
1. Admin Login
2. User Login
3. User Signup
0. Exit
```

### Admin Menu

```
1. Add Book
2. Display Books
3. Search Book
4. Issue Book
5. Return Book
6. Count Books
0. Logout
```

### User Menu

```
1. Display Books
2. Search Book
0. Logout
```

---

## ⚠️ Limitations

* Fixed-size arrays (no dynamic memory)
* No encryption for passwords
* Date calculation is approximate (30/31 day logic)
* No GUI (CLI-based system)
* Hardcoded file paths

---

## 💡 Future Improvements

* Add GUI (using C++/Qt or web interface)
* Implement database (MySQL / SQLite)
* Improve date handling (leap years, accurate months)
* Add book categories & filters
* Password hashing for security
* Multi-user concurrency support

---

## 📌 Sample Data Included

* 40+ books across genres (Programming, Fiction, Finance, etc.) 
* Multiple student accounts 
* Real issue/return records with fines 


