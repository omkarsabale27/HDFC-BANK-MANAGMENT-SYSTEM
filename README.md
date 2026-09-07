# HDFC-BANK-MANAGMENT-SYSTEM
# 🏦 HDFC_BANK_MANAGEMENT_SYSTEM

<div align="center">

# 🏦 HDFC Bank Management System

**A C++ Object-Oriented Banking Application for Account and Fund Management**

![Language](https://img.shields.io/badge/Language-C%2B%2B-blue?style=for-the-badge\&logo=cplusplus)
![Concept](https://img.shields.io/badge/Concept-OOP-brightgreen?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Linux-orange?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Complete-success?style=for-the-badge)

</div>

---

## 📌 Overview

The **HDFC Bank Management System** is a console-based banking application developed using **C++ and Object-Oriented Programming concepts**. The system simulates basic banking operations such as account creation, deposits, withdrawals, balance enquiry, account information, and fund transfer between two accounts.

The project demonstrates practical implementation of **classes, objects, encapsulation, member functions, reference passing, conditional validation, and data handling**.

> 💡 This project provides a simple real-world example of applying C++ OOP concepts to a banking application.

---

## ✨ Features

| Feature                      | Description                                                       |
| ---------------------------- | ----------------------------------------------------------------- |
| 🏦 **Account Creation**      | Creates a new bank account with customer name and initial deposit |
| 🔢 **Account Number**        | Automatically generates a 6-digit account number                  |
| 💰 **Deposit**               | Adds money to the customer's account                              |
| 💸 **Withdrawal**            | Withdraws money after checking available balance                  |
| 💳 **Fund Transfer**         | Transfers money from one account to another                       |
| 📊 **Balance Enquiry**       | Displays the current account balance                              |
| 👤 **Account Information**   | Displays account holder details and account number                |
| ✅ **Transaction Validation** | Prevents invalid transactions and insufficient-balance transfers  |
| 🖥️ **Console Interface**    | Simple and user-friendly terminal-based output                    |

---

## 🏗️ System Architecture

```text
                 HDFC BANK SYSTEM
                        │
                        ▼
              ┌───────────────────┐
              │    HDFC Class     │
              └─────────┬─────────┘
                        │
        ┌───────────────┼────────────────┐
        ▼               ▼                ▼
   Account Creation   Transactions    Account Info
        │               │                │
        ▼               ▼                ▼
   Name + Deposit   Deposit/Withdraw   Acc No + Balance
                        │
                        ▼
                  Fund Transfer
                        │
                ┌───────┴───────┐
                ▼               ▼
           Sender Account   Receiver Account
                │               │
                └───────┬───────┘
                        ▼
                 Updated Balances
```

---

## 🧩 OOP Concepts Used

### 1️⃣ Class & Objects

The `HDFC` class represents a bank account, while objects such as `myacc` and `facc` represent individual accounts.

```cpp
HDFC myacc, facc;
```

### 2️⃣ Encapsulation

Account information such as:

```cpp
int accno;
char name[30];
float bal;
```

is maintained inside the class.

### 3️⃣ Member Functions

The class provides functions for banking operations:

```cpp
CreateAcc()
Deposit()
WithDrawal()
BalEnq()
AccInfo()
Transaction()
```

### 4️⃣ Reference Passing

The transaction function uses a reference to directly update the receiver account:

```cpp
bool Transaction(HDFC &FACC)
```

### 5️⃣ Conditional Validation

The system verifies the available balance before withdrawal and fund transfer.

```cpp
if(amt > 0 && amt <= bal)
```

---

## 💰 Banking Operations

### Account Creation

```text
Enter Account Holder Name : Omkar
Enter Initial Deposit     : 10000

Account Created Successfully!
Account Number : 583421
Initial Balance: Rs.10000
```

### Fund Transfer

```text
Sender Balance   : Rs.10000
Transfer Amount  : Rs.2500
Receiver Balance : Rs.5000

Transaction Successful!

Sender Balance   : Rs.7500
Receiver Balance : Rs.7500
```

---

## ⚙️ How It Works

### 1️⃣ Account Initialization

```text
Program Start
     ↓
Create Sender Account
     ↓
Enter Name & Initial Deposit
     ↓
Generate Account Number
```

### 2️⃣ Receiver Account

```text
Create Receiver Account
     ↓
Enter Name & Initial Deposit
     ↓
Generate Account Number
```

### 3️⃣ Fund Transfer

```text
Enter Transfer Amount
          ↓
Check Available Balance
          ↓
     ┌────┴────┐
     │         │
   Valid     Invalid
     │         │
     ▼         ▼
Deduct      Transaction
Sender      Failed
Balance
     │
     ▼
Add Amount to
Receiver Balance
     │
     ▼
Transaction Successful
```

---

## 📁 Project Structure

```text
HDFC-Bank-Management-System/
│
├── HDFC.cpp
│
├── README.md
│
└── HDFC_Bank_Management_System.pdf
```

---

## 🛠️ Development Environment

| Tool                    | Details                              |
| ----------------------- | ------------------------------------ |
| **Language**            | C++                                  |
| **Programming Concept** | Object-Oriented Programming          |
| **Compiler**            | GCC / G++                            |
| **Platform**            | Linux / Windows                      |
| **Libraries**           | iostream, cstring, cstdlib, unistd.h |

---

## 🚀 Getting Started

### Prerequisites

* C++ compiler installed
* GCC / G++ compiler
* Linux terminal or Windows command prompt

### Compile

```bash
g++ HDFC.cpp -o HDFC
```

### Run

```bash
./HDFC
```

For Windows:

```bash
HDFC.exe
```

---

## 📊 Sample Output

```text
========================================
          HDFC BANK SYSTEM
========================================

>>> Creating Sender Account...

====================================
        CREATE BANK ACCOUNT
====================================

Enter Account Holder Name : Omkar
Enter Initial Deposit     : 10000

Account Created Successfully!
Account Number : 583421
Initial Balance: Rs.10000

>>> Creating Receiver Account...

====================================
        CREATE BANK ACCOUNT
====================================

Enter Account Holder Name : Rahul
Enter Initial Deposit     : 5000

Account Created Successfully!
Account Number : 724315
Initial Balance: Rs.5000

------------------------------------
         ACCOUNT INFORMATION
------------------------------------

Account Holder : Omkar
Account Number : 583421
Balance        : Rs.10000

------------------------------------
         ACCOUNT INFORMATION
------------------------------------

Account Holder : Rahul
Account Number : 724315
Balance        : Rs.5000

========================================
          FUND TRANSFER
========================================

Enter Amount to Transfer : Rs.2500

Transaction Successful!
Transferred Amount : Rs.2500

*** Transaction Completed Successfully ***

========== FINAL BALANCE ==========

Sender Account:
Account Balance : Rs.7500

Receiver Account:
Account Balance : Rs.7500
```

---

## 🎯 Project Objective

The main objective of this project is to develop a basic banking application while gaining practical knowledge of **C++ Object-Oriented Programming, classes and objects, encapsulation, functions, reference variables, conditional statements, and real-world transaction logic**.

---

## 📚 Key Learning Outcomes

* Understanding **C++ classes and objects**
* Implementing **encapsulation**
* Working with **member functions**
* Passing objects using **references**
* Implementing banking transaction logic
* Performing input validation
* Managing multiple account objects
* Developing a structured console application

---

<div align="center">

### 🏦 HDFC Bank Management System

**Built with ❤️ using C++ & Object-Oriented Programming**

</div>

