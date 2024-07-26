# Transfer Through The Same Bank Without Pin

## /api/v1.0/transfer

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request 
```json
{
    "recipientAccountNumber": "string",
    "recipientAccountName": "string",
    "amount": float64

}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "funds successfully send",
  "data": null
}
```