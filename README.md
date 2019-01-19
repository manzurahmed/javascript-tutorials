# Javascript-Tutorials

## 002 বিগিনিং জাভাস্ক্রিপ্ট - পর্ব ২, বিভিন্ন রকমের ডেটা

```js
var myName = "Earth"
```

এক লাইনে একাধিক ভ্যারিয়েবল ডিক্লেয়ার করা

```js
var a = 12, b = 13, c = 14;
```

**নোট**: ভ্যারিয়েবলের নাম **caseSensitive**.

## 005 বিগিনিং জাভাস্ক্রিপ্ট পর্ব ১ - জাভাস্ক্রিপ্টে ভ্যারিয়েবল এবং ডেটা

ভ্যারিয়েবলের অর্থবহ নাম দিতে হয়। যেমনঃ

```js
var n = 123;
```
না লিখে
```js
var totalBiscuits = 123;
```
লিখলে আমার কোড দেখলে আরেকজন বুঝতে পারবে, এই ভ্যারিয়েবলের মধ্যে আসলে কিসের মান রাখা হচ্ছে।

ভ্যারিয়েবলের নামকরণের ক্ষেত্রে camelCase ব্যবহার করা একটা স্বীকৃত স্ট্যান্ডার্ড।

```js
var myVariableNameIsBig = 0;
```

Variable কে string এর সাথে concatenate করে দেখাতে চাইলে নিচের মত করে লিখতে হবেঃ

```js
var myName = 'Manzur';
var myAge = 100;
console.log("My name is", myName, "and my age is", myAge, "years.");
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৩ - কম্পিউটারে অংক কষা (এরিথমেটিক অপারেটরস)

```js
var totalEggs = 12;
var priceEgg = 4;
var totalEggPrice = totalEggs * priceEgg;
console.log("Total price of eggs is", totalEggPrice, "taka");
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৩.৫ - অপারেটর নিয়ে আরও কিছু জানার আছে (ঐচ্ছিক পর্ব)
```js
var x;
var y = 4;

x = y++;
console.log("x = ", x, "y = ", y);

Output: x =  4 y =  5
```
কারণ হল, x এর মান undefined। x = y++; লাইনে প্রথম y এর মান x এ অ্যাসাইন হচ্ছে। তারপরে y এর মান ১ বাড়ছে।

```js
var x;
var y = 4;
x = --y;
console.log(x, y);
Output: 3 3
```

## ডাটা টাইপ

1. string
2. number
3. boolean
4. undefined
5. null

যখন কোন ভ্যারিয়েবল ডিক্লেয়ার করা হয়েছে, কিন্তু, ভ্যালু এ্যাসাইন করা হয়নি। তখন এই ইরর দেখাবে।
```
null
symbol (ES6)
```
কোন ভ্যারিয়েবলের ডাটা টাইপ জানতে ব্যবহার করতে হবে **typeof**.
```js
console.log( typeof(myName) );
```

### কনস্ট্যান্ট

কনস্ট্যান্ট ডিক্লেয়ার করতে const কিওয়ার্ড ব্যবহার করা হয়।

### এ্যাসাইনমেন্ট

```js
var x = 2;
var y = x++;

console.log(x, y);

Output: 3 2
```


