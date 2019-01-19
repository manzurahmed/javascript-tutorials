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

