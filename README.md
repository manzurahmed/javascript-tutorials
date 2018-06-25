# Javascript-Tutorials

### ভ্যারিয়েবল তৈরী করতে

```
var myName = "Earth"
```

এক লাইনে একাধিক ভ্যারিয়েবল ডিক্লেয়ার করা

```
var a = 12, b = 13, c = 14;
```

**নোট**: ভ্যারিয়েবলের নাম **caseSensitive**.

## ডাটা টাইপ

string
number
boolean
undefined যখন কোন ভ্যারিয়েবল ডিক্লেয়ার করা হয়েছে, কিন্তু, ভ্যালু এ্যাসাইন করা হয়নি। তখন এই ইরর দেখাবে।
null
symbol (ES6)

কোন ভ্যারিয়েবলের ডাটা টাইপ জানতে ব্যবহার করতে হবে **typeof**.

console.log( typeof(myName) );

### কনস্ট্যান্ট

কনস্ট্যান্ট ডিক্লেয়ার করতে const কিওয়ার্ড ব্যবহার করা হয়।

### পর্ব ৫ - লুপ

**while loop**
জাভাস্ক্রিপ্টে ৩ ভাবে লুপ লেখা যায়, do while, while, এবং, for ব্যবহার করে

```js
var counter = 10;

while(counter-- > 0)
{
    console.log(counter);
}
```

```js
var i = 0;
while (i < 20)
{
	i++;
	console.log( i );
}
```

counter এর নাম নির্দিষ্ট ভ্যালু তে পৌঁছালে break; ব্যবহার করে while থেকে বের হয়ে আসা যায়।

