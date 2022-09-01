# Documentation

API Documentation for RbxPlug.

## Table of Contents

* [Users](./USERS.MD)
* [Offers](./OFFERS.MD)
* [Postback](./POSTBACK.MD)
* [Promocodes](./PROMOCODES.MD)
* [Roblox](./ROBLOX.MD)
* [Giveaway](./GIVEAWAY.MD)
* [Lootboxes](./LOOTBOXES.MD)
* [Socials](./SOCIALS.MD)
* [Withdraw](./WITHDRAW.MD)
* [Admin](./ADMIN.MD)

## Example

### POST

```javascript
// npm install node-fetch@2
const fetch = require("node-fetch");
const server = `https://api.rbxplug.gg`;
const start = new Date().getTime();

fetch(`${server}/users/login/jub0t`, {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ refer: 1 }), // Post Data goes in Body
})
  .then((res) => res.json())
  .then((data) => {
    console.log(`${new Date().getTime() - start} Millisenconds`);
    console.log(data);
  })
  .catch((err) => {
    console.log(err);
  });
```

### GET

```javascript
// npm install node-fetch@2
const fetch = require("node-fetch");
const server = `http://127.0.0.1:3000`;

fetch(`${server}/users/avatar/1877006416`, {
  method: "GET",
  headers: { "Content-Type": "application/json" },
})
  .then((res) => res.json())
  .then((data) => {
    console.log(data);
  })
  .catch((err) => {
    console.log(err);
  });
```