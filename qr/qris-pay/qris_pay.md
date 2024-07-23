# Login Information

## /api/v1.0/qr/qr-pay
### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request paramenters
|Key            |Type               |Default    | Description | 
|---            |---                |---        | ---         |
|mode           |string             |bright     | QR display mode |

### Request 
#### JSON
```
{
  "amount": "number
}
```

### Response (200) 
#### JSON
```
{
  "status": "Success",
  "message": "QR code generated successfully",
  "data": {
    "qrImage": "string,
    "expiresAt": "string"
  }
}
```

### Inside qrImage data 
#### JSON
```
{ 
  "beneficiary": {
    "name": "string"
    "username": "string",
    "accountNumber": "string"
  },
  "amount": "number",
  "type": "QRIS Pay",
  "expiresAt": "string|datetime"
}
```