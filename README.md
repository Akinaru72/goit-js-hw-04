# Homework №4

1. Create a repository `goit-js-hw-04`.
2. Create a separate `.js` file for each task.
3. Read each task and complete it in your code editor.
4. Make sure the code is formatted using Prettier and that there are no errors or warnings in the console when opening the live task page.
5. Submit the homework for review.

Submission format: The homework should include two links — to the source files and the live GitHub Pages page.

---

## Task 1. Packing Products

Write a function `isEnoughCapacity(products, containerSize)` that calculates whether all products will fit into a container.

### Function parameters:

- `products` — an object where keys are product names and values are the quantity of each product. For example, `{ apples: 2, grapes: 4 }`.
- `containerSize` — a number representing the maximum number of product units the container can hold.

The function should return `true` if all products fit into the container, and `false` if not.

### Test code

```js
console.log(isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)); // true
console.log(isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)); // false
console.log(isEnoughCapacity({ apples: 1, lime: 5, tomatos: 3 }, 14)); // true
console.log(isEnoughCapacity({ apples: 18, potatos: 5, oranges: 2 }, 7)); // false
```

Keep this code for mentor review.

### What the mentor will pay attention to:

- The function `isEnoughCapacity(products, containerSize)` is declared
- The call `isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)` returns `true`
- The call `isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)` returns `false`
- The call `isEnoughCapacity({ apples: 1, lime: 5, tomatos: 3 }, 14)` returns `true`
- The call `isEnoughCapacity({ apples: 18, potatos: 5, oranges: 2 }, 7)` returns `false`

---

## Task 2. Calorie Calculation

Write a function `calcAverageCalories(days)` that returns the average daily number of calories consumed by an athlete during the week. The function expects one parameter: `days` — an array of objects. Each object describes a day of the week and the number of calories `calories` consumed by the athlete on that day.

Use the code below and place it after your function declaration to check its correctness.  
The console will display the results of the function calls.

```js
console.log(
  calcAverageCalories([
    { day: "monday", calories: 3010 },
    { day: "tuesday", calories: 3200 },
    { day: "wednesday", calories: 3120 },
    { day: "thursday", calories: 2900 },
    { day: "friday", calories: 3450 },
    { day: "saturday", calories: 3280 },
    { day: "sunday", calories: 3300 },
  ])
); // 3180

console.log(
  calcAverageCalories([
    { day: "monday", calories: 2040 },
    { day: "tuesday", calories: 2270 },
    { day: "wednesday", calories: 2420 },
    { day: "thursday", calories: 1900 },
    { day: "friday", calories: 2370 },
    { day: "saturday", calories: 2280 },
    { day: "sunday", calories: 2610 },
  ])
); // 2270

console.log(calcAverageCalories([])); // 0
```

Keep this code for mentor review.

### What the mentor will pay attention to:

- The function `calcAverageCalories(days)` is declared
- The call to `calcAverageCalories([...])` returns `3180`

  ```js
  calcAverageCalories([
    { day: "monday", calories: 3010 },
    { day: "tuesday", calories: 3200 },
    { day: "wednesday", calories: 3120 },
    { day: "thursday", calories: 2900 },
    { day: "friday", calories: 3450 },
    { day: "saturday", calories: 3280 },
    { day: "sunday", calories: 3300 },
  ]);
  ```

  - The call to `calcAverageCalories([...])` returns `2270`

  ```js
  calcAverageCalories([
    { day: "monday", calories: 2040 },
    { day: "tuesday", calories: 2270 },
    { day: "wednesday", calories: 2420 },
    { day: "thursday", calories: 1900 },
    { day: "friday", calories: 2370 },
    { day: "saturday", calories: 2280 },
    { day: "sunday", calories: 2610 },
  ]);
  ```

  - The call to `calcAverageCalories([])` returns `0`

  ```js
  calcAverageCalories([]);
  ```

  ***

  ## Task 3. Player Profile

The `profile` object describes a user's profile on a gaming platform. Its properties include the profile name `username` and the number of active hours `playTime` spent in the game.

```js
const profile = {
  username: "Jacob",
  playTime: 300,
};
```

Extend the `profile` object with methods to work with its properties

Method `changeUsername(newName)`

- Accepts a string (new name) as the parameter `newName`
- Changes the value of the `username` property to the new name
- Returns nothing

Method `updatePlayTime(hours)`

- Accepts a number (hours) as the parameter `hours`
- Increases the `playTime` property by this number
- Returns nothing

Method `getInfo()`

- Returns a string in the format `<Username> has <amount> active hours!`, where  
  `<Username>` — the profile's username,  
  `<amount>` — the number of active hours

Example usage

```js
console.log(profile.getInfo()); // "Jacob has 300 active hours!"

profile.changeUsername("Marco");
console.log(profile.getInfo()); // "Marco has 300 active hours!"

profile.updatePlayTime(20);
console.
```

---

**Live page: [GitHub Pages](https://akinaru72.github.io/goit-js-hw-04/)**
