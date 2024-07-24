# Login Information

## /api/v1.0/auth/login-info
### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request 
#### JSON
```
-
```

### Response (200) 
#### JSON
```
{
  "status": "success",
  "message": "success getting login information",
  "data": {
      "lastSuccessfullLoginAttempt": {
        "timestamp": "string", 
        "location": "string",
      },
      "failedLoginAttempt": {
        "timestamp": "string", 
        "location": "string",
      }
  }
}
```
