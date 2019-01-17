# ফাংশন

## 7 ফাংশনের সাথে পরিচয়  কি এবং কেন

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
