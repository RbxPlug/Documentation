# Roblox

## /roblox/user-passes `GET`

Get all of the user passes for a user. Try to send less request per client(user) as the server has a rate limitter on this endpoint.

## /roblox/create-token-phrase `POST`

Create a super token. You'll need to save `VToken` in `localStorage` or somewhere where it can be accessed later. The `Phrase` is the sentence the users will have to set as their bio, You can use the `.join(" ")` method to put the sentence together since it's an array(`string[]`).

```json
{
    "Message": "Success",
    "Data": {
        "Phrase": ["Crown", "Crown", "Tower", "Tower", "Dragon", "Bubble", "Prize", "King", "Toy", "Toy", "King", "Chip"],
        "VToken": "RImNyifJetFtwWZjp0UK0pCsfvBNYw9KSsXBS8sbMVazqTzN"
    },
    "Success": false
}
```

## /roblox/get-super-token `GET`

* roblox/get-super-token?`user_id`=1&`vtoken`=sHVvNMrs8KaIeffXiBxdLwOpTleUqnEYT5ASmOkRUzMAdEv4

The server will check for the user's bio via the Roblox user information API, and verify some other things. If everything is good the server will return `Response 200` with the `super_token`.

```json
{
    "Message": "Verified Token",
    "Data": {
        "Token": "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx",
    },
}
```

