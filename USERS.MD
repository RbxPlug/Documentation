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


## `/users/info/:username`

Get user's information, will not work if user does not exists in the database. The response is really quick(4ms record).

```js
fetch(`/users/info/jub0t`)
  .then((res) => res.json())
  .then((data) => {
    console.log(data)
  })
  .catch((err) => {
    console.log(err)
  })
```

## `/users/avatar/:user_id` `GET`

Get user's avatar information in json, if you want direct image you can put `?format=png` in the url.

```
http://127.0.0.1:3000/users/avatar/1877006416
```

