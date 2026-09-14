# Simple Bank System

A simple banking application built with **Python Object-Oriented Programming (OOP)** and **Gradio**.

The project demonstrates how to use Python classes, objects, class attributes, instance attributes, properties, methods, and basic data validation to build a simple bank account management system with a graphical web interface.

## Features

* Create a new bank account
* Store account information
* Display all created accounts
* Show the total number of accounts
* Deposit money into an account
* Withdraw money from an account
* Prevent withdrawals when the balance is insufficient
* Validate account and transaction inputs
* Interactive web interface using Gradio

## Technologies Used

* **Python** — Main programming language
* **Object-Oriented Programming (OOP)** — Used to structure the banking system
* **Gradio** — Used to create the web-based user interface

## Project Structure

```text
simple-bank-system/
│
├── app.py
├── requirements.txt
└── README.md
```

> Make sure to save the Python code as `app.py`.

## Object-Oriented Programming Concepts

This project demonstrates several important Python OOP concepts.

### Class

The `BankAccount` class represents a bank account.

```python
class BankAccount:
```

### Instance Attributes

Each account has its own:

* Name
* Email
* Balance

```python
self.name = name
self.email = email
self._balance = balance
```

### Class Attribute

The `account_count` class attribute keeps track of the total number of accounts created.

```python
account_count = 0
```

### Constructor

The `__init__()` method initializes a new bank account.

```python
def __init__(self, name, email, balance):
```

### Property

The `@property` decorator provides controlled access to the account balance.

```python
@property
def balance(self):
    return self._balance
```

### Methods

The class contains methods for performing banking operations:

* `deposit()`
* `withdraw()`
* `display_account()`

## How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/simple-bank-system.git
```

Replace `YOUR_USERNAME` with your GitHub username.

### 2. Open the Project Folder

```bash
cd simple-bank-system
```

### 3. Create a Virtual Environment

It is recommended to use a Python virtual environment.

```bash
python -m venv .venv
```

### 4. Activate the Virtual Environment

#### Windows

```bash
.venv\Scripts\activate
```

### 5. Install Dependencies

```bash
pip install -r requirements.txt
```

### 6. Run the Application

```bash
python app.py
```

Gradio will provide a local URL where you can open the application in your browser.

## How It Works

### Create Account

Enter:

* Name
* Email
* Initial balance

Then click **Create Account**.

The account is created and stored in the application's `accounts` list.

### View Accounts

The **Accounts** tab allows you to:

* Display all created accounts
* Display the total number of accounts

### Transactions

The **Transactions** tab allows you to:

* Select an account number
* Enter an amount
* Deposit money
* Withdraw money

The application checks whether the transaction is valid before modifying the account balance.

## Example

Suppose three accounts are created:

```text
===== Account 1 =====
Name: Mohamed
Email: mohamed@example.com
Balance: $1000.00

===== Account 2 =====
Name: Ahmed
Email: ahmed@example.com
Balance: $500.00
```

If `$200` is deposited into Account 1:

```text
$200.00 deposited successfully.
Current balance: $1200.00
```

If a user tries to withdraw more money than the available balance, the application returns an insufficient balance message.

## Important Note

This project is an educational banking simulation. It does **not** connect to a real bank, database, payment system, or financial institution.

Account data is stored temporarily in memory and will be lost when the application stops.

## Future Improvements

Possible improvements include:

* Add a unique account ID
* Add account passwords or authentication
* Store accounts in a database such as MySQL
* Add transaction history
* Add transfer money functionality
* Add account deletion
* Add account search
* Improve the Gradio user interface
* Add database persistence
* Add automated tests
* Add proper logging and error handling
