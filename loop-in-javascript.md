# Loop in Javascript

```js
let fruits = ["Apple", "Banana", "Mango"];
```

## 1. forEach()

forEach is an overpowered version of it’s master for loop. You start with an array let fruits = [“Apple”, “Banana”, “Mango”]
Then forEach will execute a function for each item of the list.

```js
fruits.forEach(fruit => console.log("I am eating", fruit));
 
I am eating Apple
I am eating Banana
I am eating Mango
```

## 2. map()

map is a super powerful function, and perhaps the most popular horsemen of them all.
It will take an array, manipulate the items and create a new array keeping the original array untouched.

```js
fruits.map(fruit => console.log(fruit + " is good"));

["Apple is good", "Banana is good", "Mango is good"]
```

## 3. filter()

filter has the skills of map with the power of an if statement.
It can filter out the items of your input array. After the operation, it will create a new filtered array.
Here I check to filter out only the “Apple”:

```js
fruits.filter(fruit => console.log(fruit == "Apple"));

["Apple"]
```

And here I filter only the fruits that has a length of less than 6 chars:

```js
fruits.filter(fruit => console.log(fruit.length < 6));

["Apple", "Mango"]
```

## 4. reduce()

reduce is the most powerful horsemen of the ancient one. It can be used to filter out and or combine all the items into a final single output.
Here I am making a fruit salad with all the fruits:

```js
console.log(fruits.reduce((bowl, fruit) => bowl + ", " + fruit));

"Apple, Banana, Mango"
```
