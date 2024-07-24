# QRIS Transfer

## /api/v1.0/qr/qr-tansfer
### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request paramenters
|Key            |Type      |Option         |Default    | Description | 
|---            |---       |---            |---        | ---         |
|mode           |string    |bright, dark   |bright     | QR display mode |

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
  "type": "QRIS Transfer",
  "expiresAt": "string|datetime"
}
```