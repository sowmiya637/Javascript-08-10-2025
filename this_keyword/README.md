#  Food Delivery App — "this" Keyword Demo

A **JavaScript project** demonstrating how the `this` keyword behaves in different contexts: global, object, function, class, and arrow functions.  

---

##  Features

- Demonstrates `this` in **global context**.  
- Demonstrates `this` inside **object methods**.  
- Shows `this` usage in **function context** with `call`, `apply`, and `bind`.  
- Demonstrates `this` in **class context** and **arrow methods**.  
- Explains how arrow functions preserve `this` inside `setTimeout`.  
- Interactive buttons to run each example in the browser.  

---

##  Concepts Used

| Concept | Description |
|---------|-------------|
| **Global Context** | `this` points to the global object (`window` in browsers). |
| **Object Context** | `this` refers to the object calling the method. |
| **Function Context** | `this` depends on how the function is called. Can use `call`, `apply`, or `bind` to set `this`. |
| **Class Context** | Inside class methods, `this` refers to the class instance. |
| **Arrow Functions** | Arrow functions do not have their own `this`; they inherit it from the surrounding context. |
| **setTimeout** | Using arrow functions preserves `this` inside asynchronous callbacks. |

---

Example Output
Global this === window? true
Welcome to Foodie Hub located in Chennai
Sowmiya ordered Pizza
Sowmiya ordered Burger
Sowmiya ordered Pasta
Arun started delivery for Order #101
Arun is en route!
Zesto Eats app initializing...
Zesto Eats app is live now!
