# MyPostman

My Postman

## Simple solutions for calling APIs with the recent token

There are a few ways.

### A "Get Token" request + a env variable

![](image/README/get_token_01.png)

![](image/README/get_token_02.png)

username <-> client ID

password <-> client secret

![](image/README/get_token_03.png)

![](image/README/get_token_04.png)

Postman script:

```
var jsonData = JSON.parse(responseBody);
postman.setGlobalVariable("access_token", jsonData.access_token);
```

Note: based on the version, the syntax may have different variants.

![](image/README/use_token.png)

### Get token in the Postman script (in collection level)

### Get token in the Postman script (in request level)
