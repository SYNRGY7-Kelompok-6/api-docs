# QR Transfer

## /api/v1.0/qr/qr-tansfer

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request paramenters
|Key            |Type      |Option         |Default    | Description | 
|---            |---       |---            |---        | ---         |
|mode           |string    |bright, dark   |bright     | QR display mode |
|option         |string    |qr, url        |qr         | QR get image option  |

### Request 
#### JSON
```
{
  "amount": {
    "value": "number",
    "currency": "IDR",
  }
}
```

### Response (200) 
#### JSON
```
{
  "status": "Success",
  "message": "QR code generated successfully",
  "data": {
    "qrImage": "string",
    "expiresAt": "number"
  }
}
```