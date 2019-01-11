# Javascript-Tutorials

## 002 বিগিনিং জাভাস্ক্রিপ্ট - পর্ব ২, বিভিন্ন রকমের ডেটা

```
var myName = "Earth"
```

এক লাইনে একাধিক ভ্যারিয়েবল ডিক্লেয়ার করা

```
var a = 12, b = 13, c = 14;
```

**নোট**: ভ্যারিয়েবলের নাম **caseSensitive**.

## 005 বিগিনিং জাভাস্ক্রিপ্ট পর্ব ১ - জাভাস্ক্রিপ্টে ভ্যারিয়েবল এবং ডেটা

ভ্যারিয়েবলের অর্থবহ নাম দিতে হয়। যেমনঃ

```
var n = 123;
```
না লিখে
```
var totalBiscuits = 123;
```
লিখলে আমার কোড দেখলে আরেকজন বুঝতে পারবে, এই ভ্যারিয়েবলের মধ্যে আসলে কিসের মান রাখা হচ্ছে।

ভ্যারিয়েবলের নামকরণের ক্ষেত্রে camelCase ব্যবহার করা একটা স্বীকৃত স্ট্যান্ডার্ড।

```
var myVariableNameIsBig = 0;
```

Variable কে string এর সাথে concatenate করে দেখাতে চাইলে নিচের মত করে লিখতে হবেঃ

```
var myName = 'Manzur';
var myAge = 100;
console.log("My name is", myName, "and my age is", myAge, "years.");
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৩ - কম্পিউটারে অংক কষা (এরিথমেটিক অপারেটরস)

```
var totalEggs = 12;
var priceEgg = 4;
var totalEggPrice = totalEggs * priceEgg;
console.log("Total price of eggs is", totalEggPrice, "taka");
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৩.৫ - অপারেটর নিয়ে আরও কিছু জানার আছে (ঐচ্ছিক পর্ব)
```
var x;
var y = 4;

x = y++;
console.log("x = ", x, "y = ", y);

Output: x =  4 y =  5
```
কারণ হল, x এর মান undefined। x = y++; লাইনে প্রথম y এর মান x এ অ্যাসাইন হচ্ছে। তারপরে y এর মান ১ বাড়ছে।

```
var x;
var y = 4;
x = --y;
console.log(x, y);
Output: 3 3
```

## ডাটা টাইপ

```
string
number
boolean
undefined
null
```

যখন কোন ভ্যারিয়েবল ডিক্লেয়ার করা হয়েছে, কিন্তু, ভ্যালু এ্যাসাইন করা হয়নি। তখন এই ইরর দেখাবে।
null
symbol (ES6)

কোন ভ্যারিয়েবলের ডাটা টাইপ জানতে ব্যবহার করতে হবে **typeof**.

console.log( typeof(myName) );

### কনস্ট্যান্ট

কনস্ট্যান্ট ডিক্লেয়ার করতে const কিওয়ার্ড ব্যবহার করা হয়।

### এ্যাসাইনমেন্ট

```js
var x = 2;
var y = x++;

console.log(x, y);

Output: 3 2
```

### পর্ব ৫ - লুপ

**৫.১ while loop**

জাভাস্ক্রিপ্টে ৩ ভাবে লুপ লেখা যায়,
1. do while,
2. while, এবং,
3. for ব্যবহার করে

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

counter এর নাম নির্দিষ্ট ভ্যালু তে পৌঁছালে break ব্যবহার করে while লুপ থেকে বের হয়ে আসা যায়।

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৫.৩ - do while লুপ এবং break
```
var i =0;
do {
	i++;
	console.log(i);
} while(i < 10);

var i =0;
do {
	i++;
	console.log(i);

	if( 15 == i) {
		break;
	}
} while(true);
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৫.৪ - for loop, কন্ডিশন, স্টেপিং এবং ব্রেক
```
var i = 0;
for(i; i < 20; i++) {
	console.log(i);
}

for(i; i < 20; i += 2) {
	console.log(i);
}
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৫.৫ - ফর লুপে মাল্টিপল স্টেটমেন্ট এবং স্টেপিং

```
var i,j;

for(i = 0, j = 10; i <= 10; i++, j--) {
    console.log(i,j);
}
```

