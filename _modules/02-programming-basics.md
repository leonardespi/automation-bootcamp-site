---
layout: module
title: "02 Programming Basics"
permalink: /modules/02-programming-basics/
---

# Module 2 — Programming Basics for Testers

## **Syllabus***

### **Module 1: The "Why" and "How" of Programming**
* **How Programming Works:** What is a program? (Instructions for a computer). What is a programming language? (The translator). The basic idea of logic, sequence, and algorithms.
* **The Automation Landscape:** Why learn to code? Moving from manual to automated testing.
* **Languages for Automation:** A quick look at the most popular choices (Python, JavaScript, Java/C#) and **why Python is an excellent first choice** (readability, large community, powerful libraries).
* **Setup:** Installing Python, an IDE (like VS Code), and using the basic terminal.

### **Module 2: Python Fundamentals**
* **Variables and Core Data Types:** Storing information (Strings, Integers, Floats, Booleans).
* **Essential Data Structures:**
    * **Lists:** Storing ordered collections (e.g., a list of usernames).
    * **Dictionaries:** Storing key-value pairs (critical for API/JSON data).
* **Control Flow (Making Decisions):**
    * `if`, `elif`, and `else` statements (e.g., "if this element exists, then click it").
    * Comparison and Logical Operators (`==`, `!=`, `and`, `or`).
* **Loops (Repeating Actions):**
    * **`for` loops:** Iterating over lists and dictionaries (e.g., "for each test case in this file...").
    * **`while` loops:** Repeating as long as a condition is true.

### **Module 3: Building Reusable Code**
* **Functions:** The most important concept for clean tests.
    * Defining functions (`def`) to create reusable blocks (e.g., `def login(username, password):`).
    * Parameters and `return` values.
* **Introduction to OOP (Object-Oriented Programming):**
    * **Classes and Objects:** The blueprint vs. the building (e.g., a `LoginPage` class).
    * **Methods and Attributes:** Functions and variables that belong to a class (e.g., `login_page.click_submit_button()`).
* **Modules:** How to import your own files and organize your test code.

### **Module 4: The Automation Tester's Toolkit**
* **Error Handling (Writing Robust Scripts):**
    * Using `try` and `except` to handle unexpected errors gracefully (e.g., "try to find the element, except if it's not found").
* **Working with Files:**
    * Reading test data from files (e.g., a `.csv` or `.json` file).
    * Writing results to a log file.
* **Dependency Management (The "Right" Way):**
    * **Virtual Environments (`venv`):** Why they are essential for isolating project dependencies.
    * **`pip` and `requirements.txt`:** How to install libraries (like Selenium, Pytest, Requests) and share your project with others.

### **Module 5: Putting It All Together**
* **"Pythonic" Code:** Brief tips on writing clean, readable Python (f-strings, list comprehensions).
* **Interacting with the Web (Basics):**
    * Quick introduction to the `requests` library to make simple API calls (GET, POST). This shows how Python talks to other systems.
* **Connecting to a Test Framework:**
    * A 10-minute intro to **`pytest`**. Show how to write a simple test function (`def test_login_success():`) and use the `assert` keyword. This connects all the programming concepts directly to a real-world testing context.
- 

**Exercise:** Implement small functions in `exercises/01-python-fundamentals/solution.py` and add your own unit tests.