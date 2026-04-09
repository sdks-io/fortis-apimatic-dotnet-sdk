
# Device Binding Status Enum

Enables the communication of Device Binding Status between the ACS, the DS and the 3DS Requestor. For bound devices (value = 11–14), Device Binding Status also conveys the type of binding that was performed.

> 01 - Device is not bound by Cardholder
> 
> 02 - Not eligible as determined by Issuer
> 
> 03 - Pending confirmation by Cardholder
> 
> 04 - Cardholder rejected
> 
> 05 - Device Binding Status unknown, unavailable, or does not apply
> 
> 06 through 10 - Reserved for EMVCo future use (values invalid until defined by EMVCo)
> 
> 11 - Device is bound by Cardholder (device is bound using hardware / SIM internal to the Consumer Device. For instance, keys stored in a secure element on the device)
> 
> 12 - Device is bound by Cardholder (device is bound using hardware external to the Consumer Device. For example, an external FIDO Authenticator
> 
> 13 - Device is bound by Cardholder (device is bound using data that includes dynamically generated data and could include a unique device ID)
> 
> 14 - Device is bound by Cardholder (device is bound using static device data that has been obtained from the Consumer Device
> 
> 15 - Device is bound by Cardholder (Other method)
> 
> 16 through 79 - Reserved for EMVCo future use (values invalid until defined by EMVCo)
> 
> 80 through 99 - Reserved for DS use

## Enumeration

`DeviceBindingStatusEnum`

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
| `Enum15` |
| `Enum16` |
| `Enum17` |
| `Enum18` |
| `Enum19` |
| `Enum20` |
| `Enum21` |
| `Enum22` |
| `Enum23` |
| `Enum24` |
| `Enum25` |
| `Enum26` |
| `Enum27` |
| `Enum28` |
| `Enum29` |
| `Enum30` |
| `Enum31` |
| `Enum32` |
| `Enum33` |
| `Enum34` |
| `Enum35` |
| `Enum36` |
| `Enum37` |
| `Enum38` |
| `Enum39` |
| `Enum40` |
| `Enum41` |
| `Enum42` |
| `Enum43` |
| `Enum44` |
| `Enum45` |
| `Enum46` |
| `Enum47` |
| `Enum48` |
| `Enum49` |
| `Enum50` |
| `Enum51` |
| `Enum52` |
| `Enum53` |
| `Enum54` |
| `Enum55` |
| `Enum56` |
| `Enum57` |
| `Enum58` |
| `Enum59` |
| `Enum60` |
| `Enum61` |
| `Enum62` |
| `Enum63` |
| `Enum64` |
| `Enum65` |
| `Enum66` |
| `Enum67` |
| `Enum68` |
| `Enum69` |
| `Enum70` |
| `Enum71` |
| `Enum72` |
| `Enum73` |
| `Enum74` |
| `Enum75` |
| `Enum76` |
| `Enum77` |
| `Enum78` |
| `Enum79` |
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

