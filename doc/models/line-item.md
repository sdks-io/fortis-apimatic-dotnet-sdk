
# Line Item

## Structure

`LineItem`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AlternateTaxId` | `string` | Optional | Tax identification number of the merchant that reported the alternate tax amount.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `15` |
| `DebitCredit` | [`DebitCreditEnum?`](../../doc/models/debit-credit-enum.md) | Optional | Indicator used to reflect debit (D) or credit (C) transaction. Allowed values: “D”, “C”. |
| `Description` | `string` | Optional | Description of the item.<br><br>**Constraints**: *Maximum Length*: `26` |
| `DiscountAmount` | `int?` | Optional | Total discount amount applied against the line item total ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `DiscountRate` | `int?` | Optional | Discount rate for the line item ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 9999900` |
| `ProductCode` | `string` | Optional | Merchant-defined description code of the item.<br><br>**Constraints**: *Maximum Length*: `12` |
| `Quantity` | `int?` | Optional | Quantity of the item, can accept Four (4) decimal places.<br><br>**Constraints**: `<= 99999` |
| `TaxAmount` | `int?` | Optional | Amount of any value added taxes, can accept Two (2) decimal places.<br><br>**Constraints**: `>= 0`, `<= 99999999999` |
| `TaxRate` | `int?` | Optional | Tax rate used to calculate the sales tax amount, can accept 2 decimal places.<br><br>**Constraints**: `<= 999900` |
| `TaxTypeApplied` | `string` | Optional | Type of value-added taxes that are being used (Conditional If tax amount is supplied)<br><br>> This field is only required when Merchant is directed to include by Mastercard.<br><br>**Constraints**: *Maximum Length*: `4` |
| `TaxTypeId` | `string` | Optional | Indicates the type of tax collected in relationship to a specific tax amount (Conditional If tax amount is supplied)<br><br>**Constraints**: *Maximum Length*: `2` |
| `UnitCode` | `string` | Optional | Units of measurement as used in international trade. (See Codes for Units of Measurement below for unit code abbreviations)<br><br>**Constraints**: *Maximum Length*: `3` |
| `UnitCost` | `int?` | Optional | Unit cost of the item ,Can accept Four (4) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `CommodityCode` | `string` | Optional | An international description code of the individual good or service being supplied.<br><br>**Constraints**: *Maximum Length*: `12` |
| `OtherTaxAmount` | `int?` | Optional | Used if city or multiple county taxes need to be broken out separately ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 99999999999900` |

## Example (as JSON)

```json
{
  "alternate_tax_id": "1234",
  "debit_credit": "C",
  "description": "cool drink",
  "discount_amount": 10,
  "discount_rate": 11,
  "product_code": "coke12345678",
  "quantity": 5,
  "tax_amount": 3,
  "tax_rate": 0,
  "tax_type_applied": "22",
  "tax_type_id": "a1",
  "unit_code": "gll",
  "unit_cost": 10,
  "commodity_code": "cc123456",
  "other_tax_amount": 0
}
```

