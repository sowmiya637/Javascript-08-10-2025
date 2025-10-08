#  Async/Await Food Delivery Dashboard

A simple **JavaScript async/await demo ** that simulates fetching food menu and restaurant details concurrently using **Promises**, **`Promise.all()`**, and **async/await**.

---

##  Features

* Simulates **asynchronous API calls** for fetching:

  * Restaurant Menus
  * Restaurant Details (open status & rating)
* Demonstrates:

  * **Async/Await** syntax
  * **Promise.all()** for concurrency
  * **Try/Catch/Finally** for error handling
* Displays fetched data neatly in a dashboard format.

---

##  Concepts Used

| Concept                    | Description                                                          |
| -------------------------- | -------------------------------------------------------------------- |
| **Async Function**         | Allows writing asynchronous code that looks synchronous.             |
| **Await**                  | Pauses execution until a Promise is resolved.                        |
| **Promise.all()**          | Runs multiple Promises in parallel and waits until all are resolved. |
| **setTimeout()**           | Used here to simulate network delay.                                 |
| **Random success/failure** | Mimics real API behavior where requests might fail.                  |

---

##  Code Explanation

### 1. `fetchMenu(restaurant)`

Simulates an API call that returns a restaurant’s menu after a random delay (1–2 seconds).
10% chance to fail (to test error handling).

```js
async function fetchMenu(restaurant) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (Math.random() > 0.1) resolve(`${restaurant} menu: Pizza, Burger, Pasta`);
      else reject(`${restaurant} menu failed to load`);
    }, 1000 + Math.random() * 1000);
  });
}
```

### 2. `fetchRestaurantDetails(restaurant)`

Simulates fetching restaurant details like open status and rating (0.5–1.5 sec delay).

```js
async function fetchRestaurantDetails(restaurant) {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (Math.random() > 0.1) resolve(`${restaurant} is open, rating 4.5`);
      else reject(`${restaurant} details failed`);
    }, 500 + Math.random() * 1000);
  });
}
```

### 3. `loadFoodDashboard()`

Main async function that:

* Runs menu and details fetch **concurrently** using `Promise.all()`.
* Displays results or errors.
* Uses `try...catch...finally` for control flow.

```js
async function loadFoodDashboard() {
  const restaurants = ["Domino's", "McDonald's"];
  output.textContent = "Loading food data...\n";

  try {
    const menuPromises = restaurants.map(r => fetchMenu(r));
    const detailPromises = restaurants.map(r => fetchRestaurantDetails(r));

    const [menus, details] = await Promise.all([
      Promise.all(menuPromises),
      Promise.all(detailPromises)
    ]);

    // Display data
    output.textContent += "\nMenus:\n";
    menus.forEach(m => output.textContent += m + "\n");

    output.textContent += "\nRestaurant Details:\n";
    details.forEach(d => output.textContent += d + "\n");

  } catch (error) {
    output.textContent += `Error: ${error}\n`;
  } finally {
    output.textContent += "\nFood dashboard loaded!\n";
  }
}
```



##  Example Output

```
Loading food data...

Menus:
Domino's menu: Pizza, Burger, Pasta
McDonald's menu: Pizza, Burger, Pasta

Restaurant Details:
Domino's is open, rating 4.5
McDonald's is open, rating 4.5

Food dashboard loaded!
```


