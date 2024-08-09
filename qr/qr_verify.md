# QR Verify

## /api/v1.0/qr/qr-verify

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description      |
|---            |---                |---              |
|Authorization  |Bearer             |jwt token        |
|Content-Type   |application/json   |                 |


### Request 
#### JSON
```
{
  "payload": "string"
}
```

### Response (200) 
#### JSON
```
{ 
  "beneficiaryName": "string",
  "beneficiaryAccountNumber": "string",
  "remark": "QRIS Transfer",
  "expiresAt": "number"
}
```

### OR 
#### JSON
```
{ 
  "sourceName": "string",
  "sourceAccountNumber": "string",
  "beneficiaryName": "string",
  "beneficiaryAccountNumber": "string",
  "amount": {
    "value": "number",
    "currency": "IDR"
  },
  "remark": "QRIS Pay",
  "expiresAt": "number"
}
```