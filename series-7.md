# ফাংশন

## 7.0 ফাংশনের সাথে পরিচয়  কি এবং কেন

প্রোগ্রামিং এ বার বার করা হচ্ছে এমন কাজগুলোকে ফাংশন আকারে লিখে ফেলা হয়। জাভাস্ক্রিপ্টে ফাংশন লেখা খুব সহজ। ফাংশনের সাথে প্যারামিটার হিসাবে ডাটা পাঠানো যায়। নীচে একটা ফাংশনের উদাহরণ দেয়া হয়েছে।

```js
function sayHi(name) {
    if(name) {
        console.log("Hello " + name);
    } else {
        console.log("Hello, May I know your name?");
    }
    
}

sayHi("Manzur");
sayHi();
sayHi();
```

এছাড়াও ফাংশন থেকে তার কাজ শেষে অপশনালি ডাটা return করানো যায়।

```js
function isEven(number) {
    if(number % 2 == 0) {
        return true;
    }

    return false;
}

console.log(isEven(12));
console.log(isEven(14));
console.log(isEven(29));

// Output:
true
true
false
```

## 7.1 ফাংশনে কোন প্যারামিটারের ডিফল্ট ভ্যালু

ES6 এ ফাংশনের প্যারামিটারের ডিফল্ট ভ্যালু পাস করা যায়।

```js
function sayHi(name = "Anonymous") {
    console.log("Hello " + name);
}

sayHi("Manzur");
sayHi();
sayHi();

/*
Output:
Hello Manzur
Hello Anonymous
Hello Anonymous
*/
```

## 7.2 রিইউজেবল ফাংশন - স্ট্রিং রিভার্স

এবার একটি ফাংশন তৈরী করা হয়েছে যেটি একটি string প্যারামিটার হিসাবে গ্রহন করে সেটিকে উল্টিয়ে দেখাবে।
```js
function reverseString(data) {
    var rs = data.split("").reverse().join("");

    return rs;
}

var s1 = "Hello World!";
var s2 = "Manzur Ahmed";
var reversed1 = reverseString(s1);
var reversed2 = reverseString(s2);
console.log(reversed1, reversed2);
```
!dlroW olleH demhA ruznaM
```js

```

## 7.3 ফাংশনে আনলিমিটেড আর্গুমেন্ট নেয়া - স্প্রেড অপারেটর

ভ্যারিয়েবল সংখ্যজ প্যারামিটার আর্গুমেন্ট আকারে পাস করতে চাইলে ES6 স্ট্যান্ডার্ডে "...params" ব্যবহার করতে হবে। ...params হবে আর্গুমেন্টের **শেষ** প্যারামিটার। এটি একটি ES6 ফিচার এবং এই ফিচারকে spread operator বলে।

নিচের ফাংশনের Output এ 2, 4, 1 আসার কারণ হল প্রথমবার যখন dummy ফাংশনটা কল করা হয়েছে তখন a ও b এর মান হিসাবে 1 ও 4 অ্যাসাইন হয়েছে। পরবর্তী দু'টা সংখ্যা 4 ও 10 প্যারামিটার দু'টি ...params এর মান হিসাবে ব্যবহৃত হয়েছে।

```js
function dummy(a,b, ...params) {
    console.log(params.length);
    console.log(params);
}
dummy(1,4,8,10);
dummy(1,4,6,10,12,13);
dummy(1,3,5);

/*
Output:
2
[ 8, 10 ]
4
[ 6, 10, 12, 13 ]
1
[ 5 ]
*/
```

**রিয়েল ওয়ার্ল্ড প্রবলেম**

```js
function addStudents(storage, ...people) {
    for(var i = 0; i < people.length; i++) {
        storage.push(people[i]);
    }
}

var students = [];
addStudents(students, "Mr. One", "Mr. Two", "Mr. Three");
console.log(students.length);
addStudents(students, "Mr. Four", "Mr. Eight");
console.log(students.length);
addStudents(students, "Mr. Eleven");
console.log(students.length);

/*
3
5
6
*/
```

লক্ষ্যনীয় যে, ...params এর ভ্যালুগুলো ফাংশনের মধ্যে **array** আকারে পাওয়া যায়।

## 7.4 ফাংশনের আর্গুমেন্ট ভার্সেস প্যারামিটার - কোনটা কি?

পারামিটার হলঃ একটি ফাংশন ডিক্লেয়ার করার সময় "যে কয়টি ভারিয়েবল এই ফাংশনের মধ্যে পাস করার হচ্ছে বলে ডিক্লেয়ার করা হয়", ঐ ভারিয়েবল বা ভ্যারিয়েবলগুলোকে প্যারামিটার বলা হয়।

আর্গুমেন্ট হলঃ ঐ ফাংশনকে যখন কল করা হয়, তখন ঐ ফাংশনের ভ্যারিয়েবল বা ভ্যারিয়েবল্গুলোর মান পাস করা হয়। এই মান বা মানগুলোকে আর্গুমেন্ট বলে।

## 7.5 জাভাস্ক্রিপ্ট ফাংশনে ভ্যারিয়েবল স্কোপ

কোন ভ্যারিয়েবলের মান কোন ক্ষেত্রে কি রকম থাকবে, বা, যেখান ব্যবহার করা হচ্চ্যে, তা আসলেই ব্যবহার করা যাবে কিনা, "scope" এর মাধ্যামে সেটা বোঝা যায়।

### অতীব জরুরী
Global scope এ ডিক্লেয়ার করা একটি ভ্যারিয়েবলকে ফাংশনের ভিতর থেকে ঐ একই নামে পরিবর্তন করলে গ্লোবাল ভ্যারিয়েবলের মান পরিবর্তন হয়ে যাবে।

```js
var i = 12;

// Changing the value of the variable inside this function with same name
function doSomething(){
    i = 10;
    console.log("Inside function. Changing Global scope:", i);
}

// Call function where i = 10
doSomething();
// Now call the global variable.
// Value of "i" is now 10,
```

কিন্তু, doSomething ফাংশনের মধ্যে যদি নতুন করে i নামের ভ্যারিয়েবলকে ডিক্লেয়ার করা হত, তবে Global scope এর i এর মান অপরিবর্তিত থাকত।

```js
function doSomethingElse(){
    var i = 37;
    console.log("Inside function. Changing Local scope:", i);
}
doSomethingElse();
```

### Variable Hoising

ফাংশনের মধ্যে যেখানেই ভ্যারিয়েবল ডিক্লেয়ার করা হোক না কেন, স্ক্রিপ্ট রান করার সময় জাভাস্ক্রিপ্ট ভ্যারিয়েবলগুলোকে উপরে নিয়ে আসে। এই প্রক্রিয়াকে Variable Hoisting বলে।

```js
function doVariableHoisting(){
    i = 29;
    console.log("Inside function. Variable hoisting:", i);
    // During runtime, variable i will be moved to the top
    // acting as local variable.
    var i;
}
doVariableHoisting();
```

### let এর ব্যবহার

নীচের দুইটা উদাহরণের মাধ্যমে var এবং let এর পার্থক্য বুঝতে পারা যায়।

```js
// Using "var"
console.log("---");
function doInsideVar(){
    var i = 37;

    if(true) {
        var i = 76;
        console.log("Inside if with var. ", i);
    }
    console.log("Inside function. Changing Local scope:", i);
}
doInsideVar();

// Using "let"
console.log("---");
function doInsideLet(){
    let i = 37;

    if(true) {
        let i = 76;
        console.log("Inside if with var. ", i);
    }
    console.log("Inside function. Changing Local scope:", i);
}
doInsideLet();
```

তাহলে, doInsideVar() এবং doInsideLet() ফাংশন দু'টির মাধ্যমে var এবং let ব্যবহারে ভ্যারিয়েবলের মান'কে কিভাবে প্রভাবিত করে, তা বুঝতে পারা গেল।

**মনে রাখা প্রয়োজন যে**, **let** এর স্কোপ হল, যে কোন ব্লকের মধ্যে local।
