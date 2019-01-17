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
```

