# Lootboxes

## /lootboxes/claim-free `POST`

Anyone above the rank `None` can claim a free lootbox every 24 hours. You'll need to send a `POST` request to the endpoint with the `user_id` in the request body. That's all.

## /lootboxes/list `GET`

Lists all the lootboxes you can buy.

## /lootboxes/open `POST`

Open a lootbox, Requires `lootbox_name` in body and `token`(super token) in headers.