
# Amount Ind Enum

Part of the indication whether the recurring or installment payment has a fixed or variable amount.

Starting from EMV 3DS 2.3.1:
This field is required if three_ds_requestor.three_ds_requestor_authentication_ind = 02 or 03.
This field is required if three_ri_ind= 01 or 02.

> 01 - Fixed Purchase Amount
> 
> 02 - Variable Purchase Amount
> 
> 03 through 79 - Reserved for EMVCo future use (values invalid until defined by EMVCo)
> 
> 80 through 99 - PS-specific value (dependent on the payment scheme type)

## Enumeration

`AmountIndEnum`

## Fields

| Name |
|  --- |
| `Enum01` |
| `Enum02` |
| `Enum80` |
| `Enum81` |
| `Enum82` |
| `Enum83` |
| `Enum84` |
| `Enum85` |
| `Enum86` |
| `Enum87` |
| `Enum88` |
| `Enum89` |
| `Enum90` |
| `Enum91` |
| `Enum92` |
| `Enum93` |
| `Enum94` |
| `Enum95` |
| `Enum96` |
| `Enum97` |
| `Enum98` |
| `Enum99` |

