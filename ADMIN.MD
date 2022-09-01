# Admin

## /admin/login `POST`

Requires `username` & `password` in the body.

## /admin/search-users `GET`

Use the `username` query parameter to search for users.

```
http://example.com/admin/search-users?username=jub0t
```

## /admin/add-balance `POST`

Add balance to a user's account. `username` & `amount` params in the request body are required.

## /admin/get-promocodes `GET`

List all the promocodes within the database.