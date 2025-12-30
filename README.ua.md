# Домашнє завдання №4

1. Створи репозиторій `goit-js-hw-04`.
2. Створи окремий файл із розширенням `.js` для кожної із задач.
3. Прочитай кожне завдання і виконай його в редакторі коду.
4. Переконайся, що код відформатований за допомогою Prettier, а в консолі відсутні помилки й попередження під час відкриття живої сторінки завдання.
5. Здай домашнє завдання на перевірку.

Формат здачі: Домашня робота містить два посилання: на вихідні файли та робочу сторінку на GitHub Pages.

---

## Задача 1. Пакування товарів

Напиши функцію `isEnoughCapacity(products, containerSize)`, яка обчислює, чи помістяться всі товари в контейнер при пакуванні.

### Параметри функції:

- `products` — об’єкт, у якому ключі містять назви товарів, а значення — кількість цих товарів. Наприклад, `{ apples: 2, grapes: 4 }`.
- `containerSize` — число, максимальна кількість одиниць товарів, яку може вмістити контейнер.

Функція має повернути `true`, якщо всі товари помістяться в контейнер, і `false`, якщо ні.

### Код для перевірки

```js
console.log(isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)); // true
console.log(isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)); // false
console.log(isEnoughCapacity({ apples: 1, lime: 5, tomatos: 3 }, 14)); // true
console.log(isEnoughCapacity({ apples: 18, potatos: 5, oranges: 2 }, 7)); // false
```

Залиш цей код для перевірки ментором.

### На що буде звертати увагу ментор при перевірці:

- Оголошена функція `isEnoughCapacity(products, containerSize)`
- Виклик `isEnoughCapacity({ apples: 2, grapes: 3, carrots: 1 }, 8)` повертає `true`
- Виклик `isEnoughCapacity({ apples: 4, grapes: 6, lime: 16 }, 12)` повертає `false`
- Виклик `isEnoughCapacity({ apples: 1, lime: 5, tomatos: 3 }, 14)` повертає `true`
- Виклик `isEnoughCapacity({ apples: 18, potatos: 5, oranges: 2 }, 7)` повертає `false`

---

## Задача 2. Розрахунок калорій

Напиши функцію `calcAverageCalories(days)`, яка повертає середньодобове значення кількості калорій, які спортсмен споживав протягом тижня. Функція очікує один параметр: `days` — масив об’єктів. Кожен об’єкт описує день тижня та кількість калорій `calories`, спожитих спортсменом у цей день.

Візьми код нижче і встав після оголошення своєї функції для перевірки коректності її роботи. У консоль будуть виведені результати її викликів.

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

Залиш цей код для перевірки ментором.

### На що буде звертати увагу ментор при перевірці:

- Оголошена функція `calcAverageCalories(days)`
- Виклик функції `calcAverageCalories([...])` повертає `3180`

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

- Виклик функції `calcAverageCalories([...])` повертає `2270`

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

- Виклик функції `calcAverageCalories([])` повертає `0`

```js
calcAverageCalories([]);
```

---

## Задача 3. Профіль гравця

Об’єкт `profile` описує профіль користувача на ігровій платформі. Його властивості містять ім’я профілю `username` та кількість активних годин `playTime`, проведених у грі.

```js
const profile = {
  username: "Jacob",
  playTime: 300,
};
```

### Доповни об’єкт `profile` методами для роботи з його властивостями

Метод `changeUsername(newName)`

- Приймає рядок (нове ім’я) у параметр `newName`
- Змінює значення властивості `username` на нове
- Нічого не повертає

Метод `updatePlayTime(hours)`

- Приймає число (кількість годин) у параметр `hours`
- Збільшує на нього значення властивості `playTime`
- Нічого не повертає

Метод `getInfo()`

- Повертає рядок у форматі `<Username> has <amount> active hours!`, де  
  `<Username>` — ім’я профілю,  
  `<amount>` — кількість ігрових годин

### Приклад перевірки

```js
console.log(profile.getInfo()); // "Jacob has 300 active hours!"

profile.changeUsername("Marco");
console.log(profile.getInfo()); // "Marco has 300 active hours!"

profile.updatePlayTime(20);
console.log(profile.getInfo()); // "Marco has 320 active hours!"
```

Leave this code for mentor review.

### What the mentor will check:

- The variable `profile` is declared
- The value of `profile` is an object with the properties `username`, `playTime`, `getInfo`, `changeUsername`, and `updatePlayTime`
- The property `getInfo` is a function
- The property `changeUsername` is a function
- The property `updatePlayTime` is a function
- Inside the object's methods, `this` is used to access the object's properties

---

**Жива сторінка: [GitHub Pages](https://akinaru72.github.io/goit-js-hw-04/)**
