# How to re-use token in Postman

There are a few ways.

## A token post request + a env variable (not recommended)

![get_token_01](image/README/get_token_01.png)

![get_token_02](image/README/get_token_02.png)

username <-> client ID

password <-> client secret

![get_token_03](image/README/get_token_03.png)

![get_token_04](image/README/get_token_04.png)

![use_token](image/README/use_token.png)

## Get token in the Postman script (Recommended)

Postman script:

```dos
var jsonData = JSON.parse(responseBody);
postman.setGlobalVariable("access_token", jsonData.access_token);
```

The toke can be saved in 3 scopes for re-use purpose.

- Global level
- Collection level
- Request level

Note:

The syntax may have different variants for different Postman versions.
