# Postback

## `/postback/main`

Postback url. obtain more information and secret key from the dev(s).

```
https://example.com/postback/main?amount={amount}&user_id={user_id}&auth={secret_key}&pb_type={pb_type}
```

`pb_type` can be `json` or `integer` some websites require 0/1 response instread of status code 200.