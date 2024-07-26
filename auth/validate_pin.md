# Validate Pin

## /api/v1.0/auth/validate-pin

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request 
```json
{
    "pin": "string"
}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "pin valid",
  "data": null
}
```
