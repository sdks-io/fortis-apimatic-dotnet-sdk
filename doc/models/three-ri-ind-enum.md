
# Three Ri Ind Enum

Indicates the type of 3RI request. This data element provides additional information to the ACS to determine the best approach for handling a 3RI request.

Values 06 through 12 are accepted as well if 3DS Server initiates authentication with EMV 3DS 2.2.0 version or greater (required protocol version can be set in the preferred_protocol_version field).

Starting from EMV 3DS 2.3.1:
Required if device_channel = 03 and message_category = 01 or 02.
Values 13 and 14 can be used.

> 01 - Recurring transaction
> 
> 02 - Installment transaction
> 
> 03 - Add card
> 
> 04 - Maintain card information
> 
> 05 - Account verification
> 
> 06 - Split/delayed shipment (EMV 3DS 2.2.0 version or greater)
> 
> 07 - Top-up (EMV 3DS 2.2.0 version or greater)
> 
> 08 - Mail order (EMV 3DS 2.2.0 version or greater)
> 
> 09 - Telephone order (EMV 3DS 2.2.0 version or greater)
> 
> 10 - Whitelist status check (EMV 3DS 2.2.0 version or greater)
> 
> 11 - Other payment (EMV 3DS 2.2.0 version or greater)
> 
> 12 - Billing agreement (EMV 3DS 2.2.0 version or greater)
> 
> 13 - Device Binding status check (EMV 3DS 2.3.1 version or greater)
> 
> 14 - Card Security Code status check (EMV 3DS 2.3.1 version or greater)
> 
> 80 through 99 - PS-specific values, regardless of protocol version

## Enumeration

`ThreeRiIndEnum`

## Fields

| Name |
|  --- |
| `Enum01` |
| `Enum02` |
| `Enum03` |
| `Enum04` |
| `Enum05` |
| `Enum06` |
| `Enum07` |
| `Enum08` |
| `Enum09` |
| `Enum10` |
| `Enum11` |
| `Enum12` |
| `Enum13` |
| `Enum14` |
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

