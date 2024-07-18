# Login

## /api/v1.0/auth/login
### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request 
```
{
    "username": "string",
    "password": "string"
}
```

### Response (200) 
```
{
  "data": {
    "accessToken": "string"
  }
}
```