# Login Information

## /api/v1.0/auth/login-info

### HTTP Method : `GET`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Response (200) 
#### JSON
```json
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
