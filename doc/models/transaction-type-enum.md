
# Transaction Type Enum

Identifies the type of transaction being authenticated. The values are derived from ISO 8583. This field is required in some markets. Otherwise, the field is optional.

> 01 - Goods / Service purchase
> 
> 03 - Check Acceptance
> 
> 10 - Account Funding
> 
> 11 - Quasi-Cash Transaction
> 
> 28 - Prepaid activation and Loan

## Enumeration

`TransactionTypeEnum`

## Fields

| Name |
|  --- |
| `Enum01` |
| `Enum03` |
| `Enum10` |
| `Enum11` |
| `Enum28` |

## Example

```
01
```

