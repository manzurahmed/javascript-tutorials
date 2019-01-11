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
