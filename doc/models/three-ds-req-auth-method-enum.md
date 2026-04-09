
# Three Ds Req Auth Method Enum

Mechanism used by the Cardholder to authenticate to the 3DS Requestor. "07" and "08" are accepted as well if 3DS Server initiates authentication with EMV 3DS 2.2.0 version or greater (required protocol version can be set in the preferred_protocol_version field)

> 01 - No 3DS Requestor authentication occurred (i.e. cardholder "logged in" as guest)
> 
> 02 - Login to the cardholder account at the 3DS Requestor system using 3DS Requestor's own credentials
> 
> 03 - Login to the cardholder account at the 3DS Requestor system using federated ID
> 
> 04 - Login to the cardholder account at the 3DS Requestor system using issuer credentials
> 
> 05 - Login to the cardholder account at the 3DS Requestor system using third-party authentication
> 
> 06 - Login to the cardholder account at the 3DS Requestor system using FIDO Authenticator
> 
> 07 - Login to the cardholder account at the 3DS Requestor system using FIDO Authenticator (FIDO assurance data signed) (EMV 3DS 2.2.0 version or greater)
> 
> 08 - SRC Assurance Data (EMV 3DS 2.2.0 version or greater)
> 
> 80 through 99 - can be used for PS-specific values, regardless of protocol version

## Enumeration

`ThreeDsReqAuthMethodEnum`

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

## Example

```
04
```

