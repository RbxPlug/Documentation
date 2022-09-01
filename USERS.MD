# Users

## /users/login/:username `POST`

There is no register just login, you send a request to login. `refer` is an object in the body that only works the first time you login. refer is the id of the person who reffered you to the site.

## /users/info/:username `GET`

Get user's information, will not work if user does not exists in the database. The response is really quick(4ms record).

## /users/avatar/:user_id `GET`

Get user's avatar information in json, if you want direct image you can put `?format=png` in the url.

http://example.com/users/avatar/1877006416?format=png
