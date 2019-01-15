
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
