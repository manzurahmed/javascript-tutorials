# পর্ব ৫ - লুপ

## ৫.১ while loop

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
```js
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
```js
var i = 0;
for(i; i < 20; i++) {
	console.log(i);
}

for(i; i < 20; i += 2) {
	console.log(i);
}
```

## বিগিনিং জাভাস্ক্রিপ্ট, পর্ব ৫.৫ - ফর লুপে মাল্টিপল স্টেটমেন্ট এবং স্টেপিং

```js
var i,j;

for(i = 0, j = 10; i <= 10; i++, j--) {
    console.log(i,j);
}
```

## 5.8 ফর লুপ দিয়ে নামতা_ধারাপাত_মাল্টিপ্লিকেশন টেবিল প্রিন্ট করা

```js
var counter = 0;
var innerCounter = 1;
var whichLine = 1;

for(counter = 1; counter <= 10; counter++) {
    var output = "";
    for( innerCounter = 1; innerCounter <= 10; innerCounter++ ) {
        output += innerCounter * counter;
    }
    console.log( "Namta", counter, ":", output );
}
```
