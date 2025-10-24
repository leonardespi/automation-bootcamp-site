---
layout: module
title: "02 Programming Basics"
permalink: /modules/02-programming-basics/
---

Welcome to *Module 2: Programming Basics for Testers*!
Think of this module as the **driving school for automation**. Before you can take the sleek car of Selenium, Pytest, or Appium onto the open road of real-world projects, you need to understand **how the engine works**, **how to steer**, and **what all those buttons actually do**.

You already know how to test. You spot bugs, reproduce issues, and think critically about user journeys. What we’ll do here is teach your brain to speak the computer’s language — so instead of *telling a developer*, you can *instruct the machine yourself*.

---

## 1 - The “Why” and “How” of Programming

### **How Programming Works**

Imagine you’re explaining to a friend how to make coffee:

1. Fill the kettle with water.
2. Boil it.
3. Put coffee in the mug.
4. Pour water.
5. Stir and enjoy.

Congratulations — you just learned what is an algorithm.

A **program** is simply a list of such instructions, written in a language the computer understands. Computers are obedient, literal creatures — they do exactly what you say, nothing more, nothing less. If you forget to tell them to *boil the water*, they’ll happily pour cold water onto coffee grounds and call it a day.

Programming languages like Python are **translators** between human thinking and machine action. You express logic in a structured way, and the interpreter converts that into electrical signals the CPU can execute.

The beauty is: once you learn one, the rest are like dialects. Python might say `print` Java might say `System.out.println` but they’re both yelling the same thing — “show this on the screen!”

---

### **The Automation Landscape**

As a tester, learning to code is like upgrading from **manual screwdriver** to **power drill**.
Manual testing is irreplaceable for intuition, creativity, and UX perception. But automation helps you **scale your judgment**. It’s the bridge between *knowing what to test* and *making it happen 1000 times faster without blinking*.

Learning programming opens doors:

* You can **write scripts** that check APIs overnight.
* You can **validate UI behavior** without clicking every button.
* You can **build your own test tools** when the market doesn’t have what you need.

The future of QA isn’t just about finding bugs — it’s about building systems that **prevent them from happening**. *(This has something to do with AI as well, but we'll talk about that later)*

---

### **Languages for Automation**

There are many languages — Python, JavaScript, Java, C#, Ruby — each with its own ecosystem.
But Python is like the **LEGO of programming languages**: simple pieces that can build castles.
Its syntax is clean (`print("Hello")` feels like English), the community is huge, and the libraries (like Selenium, Requests, and Pytest) are battle-tested by thousands of testers worldwide.

In short: **Python lets you focus on testing logic, not fighting syntax.**

---

## 2 - Python Fundamentals

This is where we start coding! We’ll learn the language of automation by building small, real-world analogies.

### **Variables and Core Data Types**

Variables are like **sticky notes on a whiteboard**. You write something on one and refer to it later.

```python

username = "leo"
password = "1234"

```

The computer now remembers these until you erase or overwrite them.

* **Strings** are text (like “hello world”).
* **Integers** are whole numbers (like 7).
* **Floats** are decimals (like 3.14).
* **Booleans** are truth values (`True` or `False`).

Every test you automate manipulates data. Understanding types means you can decide what operations make sense — you wouldn’t “add” apples to oranges, and you can’t concatenate an integer with a string without a conversion.

---

### **Essential Data Structures**

Now imagine your fridge.
A **list** is the shelf where you line up items: eggs, milk, cheese.
A **dictionary** is the box of labeled jars: `{ "ketchup": "red", "mustard": "yellow" }`.

#### Lists

```python
users = ["Alice", "Bob", "Charlie"]
```

You can loop over them, add new items, or check if “Alice” is in the list. Lists are the backbone of test data — test cases, credentials, endpoints.

#### Dictionaries

```python
user = {
  "name": "Leo",
  "role": "Tester",
  "active": True
}
```

This is gold for testers because most APIs return **JSON** (which is basically Python dictionaries with different punctuation). You’ll use them daily to store and check structured responses.

---

### **Control Flow: Making Decisions**

Life is full of “if… then…” statements:

* *If it’s raining, take an umbrella.*
* *Else, wear sunglasses.*

Computers think the same way.

```python

if weather == "rainy":
    take("umbrella")
else:
    take("sunglasses")

```

As a tester, you’ll often check:

```python
if element.is_displayed():
    element.click()
```

Control flow is **the decision-making nerve** of your automation brain. Combine it with comparison (`==`, `!=`) and logical operators (`and`, `or`) to describe nuanced test logic.

---

### **Loops: Repeating Actions**

Ever brushed your teeth? You probably don’t consciously repeat “move left, move right, move left…” — your brain loops until clean.

`for` loops and `while` loops do the same for computers.

```python

for user in users: 
    print("Testing login for", user)

# users is a list like the we talked about, btw this is a comment, you can use comments to wrtite anything without worring thta the computer will listen, just be careful of use them only in one line


```

Now your test runs once for each user in your dataset — saving hours of repetitive manual work.
With a `while` loop, you can repeat until a condition changes (like retrying an API call until it succeeds).

Loops are the **automation heartbeat** — rhythmic, repetitive, tireless.

---

## 3 - Building Reusable Code

Now that you can instruct the computer, let’s make your instructions **reusable**.
Copy-pasting code is like cooking the same recipe every night from scratch. Functions are like writing it down — a cookbook you can reuse forever.

---

### **Functions: Your Superpower**

A function is a **named block of logic** that you can summon anytime.

```python
def login(username, password):
    print(f"Logging in with {username}")
```

Now, whenever you need to log in, just call:

```python
login("tester1", "1234")
```

Functions let your automation scripts grow cleanly. You can change one place (the function) and automatically improve all your tests.

Key concepts:

* **Parameters**: the inputs (like ingredients).
* **Return values**: the output (like the dish served).

Functions are **the difference between messy scripts and elegant frameworks**.

---

### **Introduction to OOP (Object-Oriented Programming)**

Imagine a house blueprint. You can build 10 houses from it — each identical in structure but independent in state.
That’s what **classes** and **objects** are.

A **class** defines behavior and attributes.
An **object** is a living instance of that class.

```python
class LoginPage:
    def __init__(self, driver):
        self.driver = driver
    
    def click_login_button(self):
        self.driver.find_element("id", "login").click()
```

You just made a **LoginPage** class. Each instance knows how to log in. This concept underpins **Page Object Models** — the professional way to structure automation frameworks.

Classes keep your code modular, testable, and human-readable — much like labeling drawers in your kitchen so you always find what you need.

---

### **Modules: Organizing Your Toolbox**

As your code grows, you’ll want separate files: one for login, one for API helpers, one for utilities.

Python lets you **import** your own modules:

```python
from helpers import login
```

This keeps projects organized and readable — a key sign of professional maturity.
Remember: good code isn’t just code that *works*; it’s code others can *understand*.

---

## 4 - The Automation Tester’s Toolkit

Now we start behaving like real engineers. Programming is not just about “making it run” — it’s about making it **reliable, predictable, and maintainable**.

---

### **Error Handling (Writing Robust Scripts)**

In real life, things go wrong. The network drops. An element disappears. The test data changes.
Without error handling, your script crashes like a domino effect.

```python
try:
    element.click()
except Exception as e:
    print("Could not click element:", e)
```

`try` and `except` are your **safety nets** — they catch errors and let your program recover gracefully instead of collapsing.

As a tester, you’ll learn to expect the unexpected — error handling gives your automation the same resilience you have when running a chaotic regression cycle before release day.

---

### **Working with Files**

Testing always revolves around **data** — input files, expected results, logs.

#### Reading data:

```python
with open("data.csv") as f:
    lines = f.readlines()
```

Now you can feed that data into your tests automatically.

#### Writing results:

```python
with open("results.txt", "w") as f:
    f.write("All tests passed!")
```

When your test suite writes logs or exports metrics, you’re bridging your automation with analytics — a crucial step for QA reporting.

---

### **Dependency Management (The “Right” Way)**

Every automation project depends on external libraries. Installing them globally is like throwing all your tools into one messy toolbox.

That’s where **virtual environments** come in.
They are like **separate workbenches** for each project — neat, isolated, independent.

To create one:

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
```

You’ll also learn to use:

* `pip install selenium`
* `pip freeze > requirements.txt`

The `requirements.txt` is your **recipe card** — anyone can recreate your exact environment by running:

```bash
pip install -r requirements.txt
```

Dependency management is the secret handshake of professional developers: “My project works on my machine — and now it works on yours too.”

---

## 5 - Putting It All Together

Now comes the magic: connecting everything you’ve learned to **real-world testing**.

---

### **“Pythonic” Code**

Being “Pythonic” means writing code that’s clean, readable, and expressive.
Instead of clutter, you use elegant tools like:

* **f-strings** for readable outputs:

  ```python
  print(f"User {username} logged in successfully.")
  ```
* **List comprehensions** for concise loops:

  ```python
  active_users = [u for u in users if u.active]
  ```

It’s like learning to plate your food beautifully — same flavor, better presentation.

---

### **Interacting with the Web (Basics)**

The `requests` library is your **phone line** to other systems. You can call an API and get data back.

```python
import requests
response = requests.get("https://api.github.com/users/octocat")
print(response.json())
```

You’ve just made your computer talk to GitHub!
Understanding APIs prepares you for **end-to-end automation** — validating that the system under test behaves correctly across layers.

---

### **Connecting to a Test Framework**

Finally, we’ll use **Pytest**, the de-facto testing framework for Python.

```python
def test_login_success():
    result = login("user", "password123")
    assert result == "Success"
```

The `assert` statement is your **truth detector** — it compares actual vs expected results.
If they differ, the test fails, producing a clear, actionable report.

Pytest also allows:

* Setup/teardown fixtures
* Parameterization (run tests with different inputs)
* Parallel execution

In short, Pytest is the **stage** where all your automation skills perform together — data, control flow, and logic, all in harmony.

---

## Capstone Exercise

In your `exercises/01-python-fundamentals/solution.py`, you’ll combine all concepts:

* Define variables for credentials.
* Create functions for login and validation.
* Handle errors gracefully.
* Log the outcomes to a file.
* Add your own **unit tests** using Pytest.

This project isn’t about memorizing syntax. It’s about **thinking like a tester-engineer**: breaking down a big task into smaller automated steps that together achieve reliability and speed.

---

## Final Thoughts

Learning programming as a tester is like learning to play an instrument when you already understand rhythm.
You already *feel* the quality of a good product — programming just gives you the **notes** to compose your own testing symphony.

Don’t rush. Every concept here is a brick. Together, they form the foundation of all advanced test automation — Selenium, Appium, Playwright, API harnesses, even AI-based testing tools.

Be patient with yourself. Typing `print("Hello World")` today might feel small, but in a few months, it becomes:

```python
pytest -n auto --html=report.html
```

And that’s when you’ll realize: you’re no longer just *testing* software — you’re *engineering quality*.

---

**By the end of this module, you will:**

* Understand programming logic and structure.
* Read and write Python confidently.
* Automate repetitive tasks safely.
* Integrate your scripts with test frameworks.
* Be ready for advanced topics like Selenium, API Testing, and Continuous Integration.

The path to becoming a true **Automation Test Engineer** starts here — where curiosity meets code, and code becomes confidence.


