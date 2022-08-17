# Promocodes

## `/promocodes/redeem`

Redeem a promocode.

```js
var url = "http://127.0.0.1:3000/promocodes/redeem";

var xhr = new XMLHttpRequest();
xhr.open("POST", url);

xhr.setRequestHeader("Content-Type", "application/json");

xhr.onreadystatechange = function () {
   if (xhr.readyState === 4) {
      console.log(xhr.status);
      console.log(xhr.responseText);
   }};

var data = `{
	"user_id": "123",
 	"promocode": "FREE99"
}`;

xhr.send(data);
```