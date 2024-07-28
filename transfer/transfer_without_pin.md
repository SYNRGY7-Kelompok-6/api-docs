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
    "beneficiaryAccountNumber": "string",
    "beneficiaryAccountName": "string",
    "amount": {
      "value": float64,
      "currency": "IDR"
    }
}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "funds successfully send",
  "data": {
    "transactionId": "string",
    "amount": float64,
    "transactionDate": "string|datetime ISO-8601",
    "beneficiaryAccountNumber": "string",
    "beneficiaryName": "string",
    "sourceAccountNumber": "string",
    "sourceName": "string"
  }
}
```