# Transfer Intra-Bank

## /api/v1.0/transfer

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description                          |
|---            |---                |---                                  |
|Authorization  |Bearer             |jwt token                            |
|X-PIN-TOKEN    |pinToken           |pinToken from validate pin endpoint  |
|Content-Type   |application/json   |                                     |

### Request 
```json
{
    "beneficiaryAccountNumber": "string",
    "remark": "string (Transfer | QRIS Transfer)",
    "desc": "string",
    "amount": {
      "value": float64,
      "currency": "IDR"
    },
}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "funds successfully send",
  "data": {
    "transactionId": "string",
    "amount": {
      "value": float64,
      "currency": "IDR"
    },
    "transactionDate": "string|datetime ISO-8601",
    "remark": "string (Transfer | QRIS Transfer)",
    "desc": "string",
    "beneficiaryAccountNumber": "string",
    "beneficiaryName": "string",
    "sourceAccountNumber": "string",
    "sourceName": "string"
  }
}
```