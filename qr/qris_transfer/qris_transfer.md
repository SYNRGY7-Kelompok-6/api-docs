# Login Information

## /api/v1.0/qr/qr-transfer
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
-
```

### Response (200) 
#### JSON
```
{
  "status": "Success",
  "message": "QR code generated successfully",
  "data": {
    "qrImage": "string,
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
  "type": "QRIS Transfer",
}
```