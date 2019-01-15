
# এ্যারে

এই সিরিজে জাভাস্ক্রিপ্টের Array নিয়ে আলোচনা করা হয়েছে। কিভাবে এ্যারে তৈরী করতে হয়, এ্যারের এলিমেন্টকে প্রদর্শন করতে হয়, এ্যারেতে নতুন এলিমেন্ট যুক্ত করা, বাদ দেয়া, রিপ্লেস করা, এ্যারের থেকে কপি করে নতুন এ্যারের বানান, ইত্যাদি বিভিন্নভাবে এ্যারে নিয়ে কাজ করার পদ্ধতি দেখানো হয়েছে।

## ৬.৫ Array splice

JS এ splice ফাংশনটা slice থেকে একটু আলাদা। splice ফাংশন মূল এ্যারে থেকে একটা অংশ বের করে আনে এবং মূল এ্যারেকে ছোট করে ফেলে।

```js
var list = [
    "sun", // 0 = -7
    "mon", // 1 = -6
    "tue", // 2 = -5
    "wed", // 3 = -4
    "thu", // 4 = -3
    "fri", // 5 = -2
    "sat", // 6 = -1
];
//
console.log(list.length);
// slice(কোন ইনডেক্স থেকে কাটা শুরু করব, কয়টা এলিমেন্ট কাটব)
//var chunk = list.splice(1, 3);
var chunkNegativeIndex = list.splice(-4, 3);
//
console.log(list.length);
//console.log(list, chunk);
console.log(list, chunkNegativeIndex);
```

আউটপুট

```js
7
4
[ 'sun', 'mon', 'tue', 'sat' ] [ 'wed', 'thu', 'fri' ]
```

## ৬.৬ এ্যারে কপি করা

```js
var list = [
    "sun", // 0 = -7
    "mon", // 1 = -6
    "tue", // 2 = -5
    "wed", // 3 = -4
    "thu", // 4 = -3
    "fri", // 5 = -2
    "sat", // 6 = -1
];

var list2 = list;
list[1] = "No day";
console.log(list, list2);
```

লক্ষ্যনীয় যে, list নামের এ্যারে থেকে list2 তে এ্যাসাইন করা হয়েছে।
পরে list এ্যারের একটা এলিমেন্টের মান পরিবর্তন করতে list2 এর এ্যারেতেও পরিবর্তন হয়ে গেছে।
কেন এমন হয়েছে, এটা বুঝতে হলে ২টি জিনিষ বুঝতে হবে।
1. Shallow copy, এবং
2. Deep copy

- Shallow copy তে ভ্যারিয়েবলের মান (value) কপি হয়।
- Deep copy তে ভ্যারিয়েবলের মান reference কপি হয়।

উদাহরন হিসাবে বলা যায়, এখানে shallow copy হয়েছে।

```js
var v1 = 2;
var v2 = v1;

v2 = 4;
console.log(v1, v2);
```

এ্যারের ক্ষেত্রে Deep copy বা reference copy হয়েছে।
তাহলে, এ্যারে কপি করতে হলে slice() ফাংশন ব্যবহার করতে হবে।

```js
var list2 = list.slice();
list[1] = "No day";
console.log(list, list2);
```

- ES6 এ কপি করতে ৩টা ডট (...) ব্যবহার করা যায়

```js
var list2 = [...list];
```

- Vanilla JS এ এ্যারে কপি করার এই কমান্ড আগে থেকেই আছে

```js
var list2 = Array.from(list);
list[1] = "No day";
console.log(list, list2);
```

## ৬.৭ একটা এ্যারের সাথে আরেকটা এ্যারে যোগ করা (Merge)

একটা এ্যারের সাথে আরেকটা এ্যারে merge করে নতুন আরেকটা এ্যারে বানাতে .concat ফাংশন ব্যবহার করা হয়।

```js
var list1 = [
	"sun",
	"mon",
	"tue",
];

var list2 = [
	"wed",
	"thu",
];

var list3 = [
	"fri",
	"sat",
];

var final = list1.concat(list2, list3);
console.log(final);
```
