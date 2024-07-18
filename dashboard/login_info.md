# Login Information

## /api/v1.0/login-info
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
