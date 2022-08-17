# Users

## `/users/login/:username`

There is no register just login, you send a request to login. `refer` is an object in the body that only works the first time you login. refer is the id of the person who reffered you to the site.

```js
var url = "http://localhost:3000/users/login/jub0t";

var xhr = new XMLHttpRequest();
xhr.open("POST", url);

xhr.setRequestHeader("Content-Type", "application/json");

xhr.onreadystatechange = function () {
   if (xhr.readyState === 4) {
      console.log(xhr.status);
      console.log(xhr.responseText);
   }};

var data = `{
	"refer": 1
}`;

xhr.send(data);
```