# Bank Statement

## /api/v1.0/bank-statement
### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

### Request parameters
|Key            |Type               |Default    | Description | 
|---            |---                |---        | ---         |
|page           |number             |0          | Pagination for detailData |
|pageSize       |number             |10         | Pagination for detailData |
|fromDate       |date               |today      | Mutation query            |
|toDate         |date               |today      | Mutation query            |

### Request 
#### JSON
```
{
    "accountNo": "string",
}
```

### Response (200) 
#### JSON
```
{
  "status": "success",
  "message": "success getting account info",
  "data": {
        "accountInfo": {
            "accountNo": "string",
            "accountType": "string",
            "accountCardExp": "string",
            "name": "string",
            "accountBalance": {
                "availableBalance": {
                  "value": float64,
                  "currency": "string(3)",
                },
                "holdAmount": {
                  "value": float64,
                  "currency": "string(3)",
                },
            },
            "accountMonthly": {
                "monthlyIncome": {
                    "value": float64,
                    "currency": "string(3)",
                },
                "monthlyOutcome": {
                  "value": float64,
                  "currency": "string(3)",
                },
            },
            "pinExpiredTimeLeft": number
         },
        "accountBalance": {
            "startingBalance": {
                "value": float64,
                "currency": "string(3)",
                "dateTime": "string|datetime ISO-8601"
            },
            "endingBalance": {
                "value": float64,
                "currency": "string(3)",
                "dateTime": "string|datetime ISO-8601"
            }
        },
        "mutations": [
            {
                "amount": {
                    "value": float64,
                    "currency": "string(3)"
                },
                "transactionDate": "string|datetime ISO-8601",
                "remark": "string",
                "type": "string(DEBIT|CREDIT)",
                "beneficiaryAccount": {
                    "beneficiaryAccountNumber": "string",
                    "beneficiaryAccountName": "string"
                },
                "sourceAccount": {
                    "beneficiaryAccountNumber": "string",
                    "beneficiaryAccountName": "string"
                },
            }
        ]
  }
}
```
