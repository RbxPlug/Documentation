# Offers 

## `/offers/leaderboard`

```js
var url = "http://127.0.0.1:3000/offers/leaderboard?length=10&offset=0";

var xhr = new XMLHttpRequest();
xhr.open("GET", url);

xhr.onreadystatechange = function () {
   if (xhr.readyState === 4) {
      console.log(xhr.status);
      console.log(xhr.responseText);
   }};

xhr.send();
```
