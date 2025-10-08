#  JavaScript Bank Account System

A simple **JavaScript OOP ** that demonstrates **classes, inheritance, methods, and static methods** to simulate a basic bank account system.  

---

##  Features

- Create **Bank Accounts** with initial balance and owner.  
- **Deposit** money into the account.  
- **Withdraw** money with balance and overdraft checks.  
- **Savings Account** supports interest calculation.  
- **Checking Account** supports overdraft limit.  
- Demonstrates **inheritance**, **method overriding**, and **static methods**.  

---

##  Concepts Used

| Concept | Description |
|----------|--------------|
| **Class** | Blueprint for creating objects with properties and methods. |
| **Constructor** | Special method to initialize object properties when created. |
| **Methods** | Functions inside classes to define behavior (deposit, withdraw, etc). |
| **Inheritance (`extends`)** | Child class inherits properties and methods from parent class. |
| **`super()`** | Calls parent class constructor from child class. |
| **Static Method** | Belongs to the class itself, not the object. Called as `ClassName.method()`. |
| **Method Overriding** | Child class can redefine parent method (e.g., `withdraw` in `CheckingAccount`). |

---

Example Output
Welcome to JS Bank!

Alice deposited $500. New balance: $1500
Alice earned $75.00 interest. New balance: $1575.00
Alice withdrew $200. New balance: $1375.00
Alice's balance: $1375

Bob withdrew $600. New balance: $-100
Bob exceeds overdraft limit!
Bob's balance: $-100

  static bankInfo() { return " Welcome to JS Bank!"; }
}
