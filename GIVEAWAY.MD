# Giveaway

## `/giveaway/info`

This will give you data for the currently running giveaway. Like the contestants, time left, duration, etc.

## `/giveaway/join`

This endpoint allows you to join the giveaway. Using the `user_id` param in the body you can join the giveaway. But in order for it to work the user must exist in the database otherwise it will return an error.

```js
var url = "http://127.0.0.1:3000/giveaway/join";

var xhr = new XMLHttpRequest();
xhr.open("POST", url);

xhr.setRequestHeader("Content-Type", "application/json");

xhr.onreadystatechange = function () {
   if (xhr.readyState === 4) {
      console.log(xhr.status);
      console.log(xhr.responseText);
   }};

var data = `{
	"user_id": "123"
}`;

xhr.send(data);
```