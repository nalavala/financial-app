# financial-app

# Endpoints :
---

## Login
**`POST /api/auth/login`**
### Request: 
```JSON
{
    "username" : "test@test.com",
    "password" : "pass123"
}
```
### Response :
```JSON
{
    "refresh_token" : "dsfasdfadfafdada",
    "access_token" : "adsfasdffadfas.asffdsfasdfadfasdfasdfa.fasdfasdfasdfasdf",
}
```

## Refresh token
**`POST /api/auth/refresh`**
### Request: 
```JSON
{
    "refresh_token" : "dsfasdfadfafdada"
}
```
### Response :
```JSON
{
    "refresh_token" : "dsfasdfadfafdada",
    "access_token" : "adsfasdffadfas.asffdsfasdfadfasdfasdfa.fasdfasdfasdfasdf",
}
```

## Signup
**`POST /api/auth/signup`**
### Request: 
```JSON
{
    "username" : "test@test.com",
    "name" : "test",
    "password" : "pass123"
    
}
```
### Response :
```JSON
{
    "user_id" : "dsfadsffa-adfasfdas-afdasfa-afsdfasd",
    "verified" : true,
}
```
## Logout
**`POST /api/auth/logout`**
