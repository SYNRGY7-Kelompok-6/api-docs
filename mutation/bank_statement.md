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

### Request 
#### JSON
```
{
    "accountNo": "string",
    "fromDateTime": "string",
    "toDateTime": "string",
}
```

### Response (200) 
#### JSON
```
{
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
        "balance": {
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
        "totalCreditEntries": {
            "numberOfEntries": number,
            "amount": {
                "value": float64,
                "currency": "string(3)"
            }
        },
        "totalDebitEntries": {
            "numberOfEntries": number,
            "amount": {
                "value": float64,
                "currency": "string(3)"
            }
        },
        "detailData": [
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
