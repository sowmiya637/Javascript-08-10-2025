#  JavaScript Promises: Fetch Users & Posts

A practical **JavaScript Promise** demonstrating how to fetch data from multiple APIs, handle asynchronous operations, and use **Promise.all()** and **Promise.race()** for concurrency.

---

##  Features

- Fetch **Users** and **Posts** from `jsonplaceholder.typicode.com`.  
- Show total **users** and **posts** fetched.  
- Display **post count for each user**.  
- Demonstrates **Promise chaining**.  
- Shows which API responds **fastest** using **Promise.race()**.  
- Error handling with `.catch()` and guaranteed completion with `.finally()`.  

---

##  Concepts Used

| Concept | Description |
|---------|-------------|
| **Promise** | Represents a value that may be available now, later, or never. |
| **Promise.all()** | Waits for multiple Promises to complete, returns results in an array. |
| **Promise.race()** | Returns the first Promise that resolves or rejects. |
| **.then()** | Executes code after a Promise is resolved. |
| **.catch()** | Handles errors if a Promise is rejected. |
| **.finally()** | Runs code regardless of success or failure. |
| **Chaining** | Passing result from one `.then()` to the next. |
| **Fetch API** | Makes HTTP requests and returns Promises. |

---

Example Output
Fetching data...
Users fetched: 10
Posts fetched: 100

User Post Count:
Leanne Graham → 10 posts
Ervin Howell → 10 posts
Clementine Bauch → 10 posts
...
Fastest API responded first!

Operation Completed!
