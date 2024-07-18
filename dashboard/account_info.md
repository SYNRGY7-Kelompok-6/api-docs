# Account Information

## /api/v1.0/account-info
### Headers
|Header         |Value              |Description|
|---            |---                |---        |
|Authorization  |Bearer             |jwt token  |
|Content-Type   |application/json   |           |

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
  "data": {
      "accountNo": "string",
      "accountType": "string",
      "accountCardExp": "string",
      "name": "string",
      "accountInfos": {
        "availableBalance": {
          "value": float64,
          "currency": "string(3)",
        },
        "holdAmount": {
          "value": float64,
          "currency": "string(3)",
        },
      },
      "accountMonthlyStats": {
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
  }
}
```
#### Description
|Key               |Description                  |
|---               |---                          |
|accountNo         |requested account number     |
|accountType       |requested account type, ex: Tahapan Xpresi     |
|accountCardExp    |requested account expiration year and month, ex : 24/7 (24th of July) |
|name              |account owner full name | 
|availableBalance  |balance that can be used for financial transaction |
|holdAmount        |hold amount that can’t be used    |
|monthlyIncome     |sum of credit transactions value in this month|
|monthlyOutcome    |sum of debit transactions value in this month|
|value             |amount of balance, ex: 50000      |
|currency          |currency of the value, ex: IDR, SGD, USD, JPY|
|pinExpiredTimeLeft|pin expired time left from 'pin_expired_date' in days|
