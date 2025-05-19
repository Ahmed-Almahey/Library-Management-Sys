# Library-Management-Sys
# 📚 Library Management System (Console-based)

A simple, console-based Library Management System written in Python, using OOP principles and JSON file handling to manage book records. This system allows users to add, update, delete, and view books in a persistent storage.

---

## 🔧 Features

- ✅ Add new books with details: name, author, year, genre, and availability  
- ✏️ Update availability of a book by name  
- ❌ Delete a book by publication year  
- 📃 Display all stored books  
- 💾 Persistent storage using `books.json`  
- 🧠 Object-Oriented Design (Classes: `Book`, `BookManager`, `FrontendManager`)  
- 🔁 Runs continuously until user exits  

---

## 🏗️ System Design

### 1. **Book Class**
Stores and represents a single book.

- **Attributes**: `name`, `author`, `year`, `genre`, `availability`  
- **Methods**:
  - `display_information()`: Print book details  
  - `to_dictionary()`: Convert object to dictionary (for JSON)

### 2. **BookManager Class**
Manages the book list and handles CRUD operations.

- **Methods**:
  - `add_book()`
  - `delete_by_year(year)`
  - `update_availability_by_name(name)`
  - `list_all_books()`
  - `save_to_file()`
  - `load_from_file()`
  - `exit_program()`

### 3. **FrontendManager Class**
Handles the user interface and menu.

- Displays menu  
- Takes user input (1–5)  
- Calls the appropriate `BookManager` method

---

## 💾 File Handling

- **File Name**: `books.json`  
- **Format**: JSON list of book dictionaries  
- Automatically loads and saves book data on start and exit.

---

## ▶️ How to Run

```bash
python main.py


## 🗂️ Project Structure

│ library-management-system/
├── books.json              # JSON file storing book records
├── book.py                 # Book class
├── book_manager.py         # BookManager class
├── frontend_manager.py     # FrontendManager class
└── main.py                 # Entry point to run the program
