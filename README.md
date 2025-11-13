# Library Management System (OOP Version)

## Project Overview
This project is a simple **Library Management System** implemented in **Python** using **Object-Oriented Programming (OOP)** principles.  
The system allows you to:

- Add books to the library
- Register library members
- Borrow and return books
- Display available books and books borrowed by members
- Handle errors for invalid operations (e.g., borrowing unavailable books or exceeding borrowing limits)

The goal of this project is to demonstrate OOP concepts such as **classes, objects, encapsulation, and interaction between objects** in a practical application.

---

## Project Structure

### library-management-oop/
- oop_solution.py   
- test_oop.py
- library_procedural.py
- test_procedural.py
- README.md

---

## Design Overview

### 1. `Book` Class
Represents a book in the library.

**Attributes:**
- `id` (int) - Unique identifier for the book
- `title` (str) - Title of the book
- `author` (str) - Author of the book
- `total_copies` (int) - Total number of copies in the library
- `available_copies` (int) - Copies currently available for borrowing

**Methods:**
- `borrow_copy()` - Reduces available copies by 1 if available; returns True if successful
- `return_copy()` - Increases available copies by 1

---

### 2. `Member` Class
Represents a library member.

**Attributes:**
- `id` (int) - Unique identifier for the member
- `name` (str) - Name of the member
- `email` (str) - Email address of the member
- `borrowed_books` (list) - List of Book objects currently borrowed

**Methods:**
- `borrow_book(book)` - Adds a book to the borrowed list if the member hasn't reached the borrowing limit (3 books max)
- `return_book(book)` - Removes a book from the borrowed list

---

### 3. `Library` Class
Represents the library system itself, managing collections of books and members.

**Attributes:**
- `books` (list) - List of all Book objects in the library
- `members` (list) - List of all Member objects
- `borrowed_books` (list) - List of dictionaries tracking borrow transactions

**Methods:**
- `add_book(id, title, author, total_copies)` - Adds a new book to the library
- `find_book(book_id)` - Searches for a book by its ID
- `add_member(id, name, email)` - Registers a new member
- `find_member(member_id)` - Searches for a member by ID
- `borrow_book(member_id, book_id)` - Handles borrowing logic
- `return_book(member_id, book_id)` - Handles returning logic
- `display_available_books()` - Prints all books with available copies
- `display_member_books(member_id)` - Prints all books currently borrowed by a specific member

---
