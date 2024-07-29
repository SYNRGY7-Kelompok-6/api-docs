# Saved Accounts

## /api/v1.0/saved-accounts

### HTTP Method : `POST`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request 
```json
{
    "beneficiaryAccountNumber": "string"
}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "account has been saved successfully",
  "data": {
      "savedBeneficiaryId": "string",
      "beneficiaryAccountNumber": "string",
      "beneficiaryAccountName": "string",
      "isFavorite": boolean
    }
}
```

## /api/v1.0/saved-accounts

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
      "savedBeneficiaryId": "string",
      "beneficiaryAccountNumber": "string",
      "beneficiaryAccountName": "string",
      "isFavorite": boolean
    },
  ]
}
```

## /api/v1.0/saved-accounts/`:savedBeneficiaryId`

### HTTP Method : `GET`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request parameters

| Key                | Type   | required | Description           | Parameter |
| -------------      | ------ | -------- | -----------           | --------- |
| savedBeneficiaryId | string | `true`   | saved beneficiary ID  | path      |

### Response (200) 
```json
{
  "status": "success",
  "message": "accounts has been retrieved successfully",
  "data": {
      "savedBeneficiaryId": "string",
      "beneficiaryAccountNumber": "string",
      "beneficiaryAccountName": "string",
      "isFavorite": boolean
    }
}
```

## /api/v1.0/saved-accounts/`:savedBeneficiaryId`

### HTTP Method : `PATCH`

### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request parameters

| Key                | Type   | required | Description           | Parameter |
| -------------      | ------ | -------- | -----------           | --------- |
| savedBeneficiaryId | string | `true`   | saved beneficiary ID  | path      |

### Request 
```json
{
    "isFavorite": boolean
}
```

### Response (200) 
```json
{
  "status": "success",
  "message": "account has been saved to favorite",
  "data": {
      "savedBeneficiaryId": "string",
      "beneficiaryAccountNumber": "string",
      "beneficiaryAccountName": "string",
      "isFavorite": boolean
    }
}
```