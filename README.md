### Coffee Shop App

Write a **class** called **CoffeeShop**, which has **three instance variables**:

1.  **name** : a string (basically, of the shop)
2.  **menu** : an array of items (of object type), with each item containing the **item** (name of the item), **type** (whether _food_ or a _drink_) and **price**.
3.  **orders** : an empty array

and **seven methods**:

1.  **addOrder**: adds the **name** of the item to the end of the **orders** array if it exists on the **menu**. Otherwise, return `"This item is currently unavailable!"`
2.  **fulfillOrder**: if the **orders** array is **not empty**, return `"The {item} is ready!"`. If the **orders** array is empty, return `"All orders have been fulfilled!"`
3.  **listOrders**: returns the list of **orders** taken, otherwise, an **empty** array.
4.  **dueAmount**: returns the total amount due for the **orders** taken.
5.  **cheapestItem**: returns the **name** of the cheapest item on the menu.
6.  **drinksOnly**: returns only the _item_  **names** of _type_  **drink** from the menu.
7.  **foodOnly**: returns only the _item_  **names** of _type_  **food** from the menu.

**IMPORTANT**: Orders are fulfilled in a **FIFO** (first-in, first-out) order.


### Examples

```
let menu = [
  {
    name: "Coffee",
    type: "drink",
    price: 1.59,
  },
  {
    name: "Sandwich",
    type: "food",
    price: 4.99,
  },
  {
    name: "Donut",
    type: "food",
    price: 2.59,
  },
  {
    name: "Coke",
    type: "drink",
    price: 1.99,
  },
  {
    name: "Lemonade",
    type: "drink",
    price: 1.99,
  },
  {
    name: "Toast",
    type: "food",
    price: 3.99,
  },
  {
    name: "Cinnamon roll",
    type: "food",
    price: 3.99,
  },
  {
    name: "Iced coffee",
    type: "drink",
    price: 3.99,
  },
];

let tcs = new CoffeeShop("Coffee Place", menu, []);


console.log(tcs.addOrder("hot cocoa")); 
console.log(tcs.addOrder("iced tea")); 

console.log(tcs.addOrder("Cinnamon roll")); 
console.log(tcs.addOrder("Iced coffee")); 
console.log(tcs.listOrders()); 

console.log(tcs.dueAmount()); 
console.log(tcs.fulfillOrder()); 
console.log(tcs.fulfillOrder()); 
console.log(tcs.fulfillOrder()); 
console.log(tcs.listOrders()); 
console.log(tcs.dueAmount()); 

console.log(tcs.cheapestItem()); 
console.log(tcs.drinksOnly()); 
console.log(tcs.foodOnly()); 
```

### Notes

Round off **due amount** up to **two decimal** places.
