# Giveaway

## /giveaway/info `GET`

This will give you data for the currently running giveaway. Like the contestants, time left, duration, etc.

## /giveaway/join `POST`

This endpoint allows you to join the giveaway. Using the `user_id` param in the body you can join the giveaway. But in order for it to work the user must exist in the database otherwise it will return an error.