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


## Create Bank
**`POST /api/vault/bank`**
### Request: 
```JSON
{
    "name" : "State Bank Of India",
    "code" : "sbi"
}
```
### Response :
```JSON
{
    "id" : "sbi_1234",
    "name" : "State Bank Of India",
    "code" : "sbi"
}
```

## Create Bank user Profile
**`POST /api/vault/bank/{bank_id}/profile`**
### Request: 
```JSON
{
    "customer_id" : "cdr34d334",
    "name_in_bank" : "Nalavala Venkata Revanth Reddy",
    "max_credit_limit" : 45665,
}
```

## Add bank account
**`POST /api/vault/bank/{bank_id}/account`**
### Request: 
```JSON
{
    "account_number" : "3454352435234234",
    "balance" : 4342.33,
    "acc_type" : "SAVINGS",
    "branch" : "Nandimandalam",
    "ifsc_code" : "SBIN00000343"
}
```
## Add card to account
**`POST /api/vault/account/{account_id}/card`**
### Request: 
```JSON
{
    "card_number" : "3454352435234234",
    "card_name" : 4342.33,
    "type" : "SAVINGS",
    "expire_date" : "09/23",
    "start_date" : "08/20"
    "cvv" : "069"
}
```

## Add/Create Demat Broker
**`POST /api/vault/demat/broker`**
### Request: 
```JSON
{
    "name" : "Zerodha Broking Limited",
    "depository" : "CDSL"
}
```
### Response: 
```JSON
{
    "id" : "zerodha_1234"
}
```

## Add/Create demat account
**`POST /api/vault/demat/{broker_id}/account`**
### Request: 
```JSON
{
    "username" : "Zerodha",
    "name" : "Nalavala Revanth Redy",
    "pan" : "BEOPN43l",
    "phone_number" : 7657766,
    "demat_id" : 12323232,
    "email" : "tet@test.com"
    "dp_id" : 12081600,
    "BO_id" : 79786115,
    "bank_account_ids" : []
}
```
