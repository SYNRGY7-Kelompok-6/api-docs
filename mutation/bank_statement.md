# Bank Statement

## /api/v1.0/bank-statement

### HTTP Method : `GET`

### Headers

| Header        | Value            | Description |
| ------------- | ---------------- | ----------- |
| Authorization | Bearer           | jwt token   |
| Content-Type  | application/json |             |

### Request parameters

| Key      | Type   | Default | Description               | Parameter |
| -------- | ------ | ------- | ------------------------- | --------- |
| page     | number | 0       | Pagination for detailData | query     |
| pageSize | number | 10      | Pagination for detailData | query     |
| fromDate | date   | today   | Mutation query            | query     |
| toDate   | date   | today   | Mutation query            | query     |

### Response (200)

#### JSON

```json
{
  "status": "success",
  "message": "success getting account info",
  "data": {
        "accountInfo": {
            "accountNo": "string",
            "accountType": "string",
            "accountCardExp": "string",
            "name": "string",
            "cvv": "string(3)",
            "balance": {
                "availableBalance": {
                  "value": float64,
                  "currency": "string(3)",
                },
                "holdAmount": {
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
                "transactionId": "string | UUID format",
                "amount": {
                    "value": float64,
                    "remainingBalance": float64,
                    "currency": "string(3)"
                },
                "transactionDate": "string|datetime ISO-8601",
                "remark": "string (Transfer | QRIS)",
                "desc": "string",
                "type": "string(DEBIT|CREDIT)",
                "beneficiaryAccount": {
                    "beneficiaryAccountNumber": "string",
                    "beneficiaryAccountName": "string"
                },
                "sourceAccount": {
                    "sourceAccountNumber": "string",
                    "sourceAccountName": "string"
                },
            }
        ]
  }
}
```

# Detail Mutation

## /api/v1.0/bank-statement/detail

### HTTP Method : `GET`

### Headers

| Header        | Value            | Description |
| ------------- | ---------------- | ----------- |
| Authorization | Bearer           | jwt token   |
| Content-Type  | application/json |             |

### Request parameters

| Key            | Type   | required | Description       | Parameter |
| -------------  | ------ | -------- | -----------       | --------- |
| id_transaction | string | `true`   | transaction ID    | query     |

### Response (200)

#### JSON

```json
{
  "status": "success",
  "message": "success getting account info",
  "data": {
            "transactionId": "string | UUID format",
            "amount": float64,
            "transactionDate": "string|datetime ISO-8601",
            "remark": "string (Transfer | QRIS)",
            "desc": "string",
            "type": "string(DEBIT|CREDIT)",
            "beneficiaryName": "string",
            "beneficiaryAccountNumber": "string",
            "sourceName": "string",
            "sourceAccountNumber": "string"
    }
}
```

# Account Monthly

## /api/v1.0/bank-statement/monthly

### HTTP Method : `GET`

### Headers

| Header        | Value            | Description |
| ------------- | ---------------- | ----------- |
| Authorization | Bearer           | jwt token   |
| Content-Type  | application/json |             |

### Request parameters

| Key      | Type   | Default       | Description            | Parameter |
| -------- | ------ | ------------  | ---------------------- | --------- |
| month    | number | currentMonth  | month number from 1-12 | query     |

### Response (200)

#### JSON

```json
{
  "status": "success",
  "message": "success getting account info",
  "data": {
        "monthlyIncome": {
            "value": float64,
            "currency": "string(3)",
        },
        "monthlyOutcome": {
            "value": float64,
            "currency": "string(3)",
        }
    }
}
```