# Postback

## /postback/main `GET`

Postback URL, `pb_type` can be `json` or `integer` some websites require 0/1 response instread of status code 200. The key for `&auth={secret_key}` is located in `.env`. 

```
https://example.com/postback/main?amount={amount}&user_id={user_id}&auth={secret_key}&pb_type={pb_type}
```
