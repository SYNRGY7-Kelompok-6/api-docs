# Saved Accounts

## /api/v1.0/saved-accounts/

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request 
```json
{
    "accountNumber": "string",
    "accountName": "string
}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "account has been saved successfully",
  "data": null
}
```

## /api/v1.0/saved-accounts/list

### HTTP Method : `GET`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |


### Response (200) 
```json
{
  "status": "success",
  "message": "accounts has been retrieved successfully",
  "data": [
    {
      "accountNumber": "string",
      "accountName": "string"
    },
  ]
}
```

## /api/v1.0/saved-accounts/`:accountNumber`

### HTTP Method : `GET`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request parameters

| Key           | Type   | required | Description     | Parameter |
| ------------- | ------ | -------- | -----------     | --------- |
| accountNumber | string | `true`   | account number  | path      |

### Response (200) 
```json
{
  "status": "success",
  "message": "accounts has been retrieved successfully",
  "data": {
      "accountNumber": "string",
      "accountName": "string"
    }
}
```