
# Terminal

Terminal Information on `expand`

*This model accepts additional fields of type object.*

## Structure

`Terminal`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LocationId` | `string` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `DefaultProductTransactionId` | `string` | Optional | Product Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `TerminalApplicationId` | `string` | Optional | Terminal Application ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `TerminalCvmId` | `string` | Optional | Terminal CVM ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `TerminalManufacturerCode` | [`TerminalManufacturerCode?`](../../doc/models/terminal-manufacturer-code.md) | Optional | - |
| `Title` | `string` | Optional | Terminal Name<br><br>**Constraints**: *Maximum Length*: `64` |
| `MacAddress` | `string` | Optional | Terminal MAC Address<br><br>**Constraints**: *Pattern*: `^([0-9a-fA-F]{2}[:-]?){5}([0-9a-fA-F]{2})$` |
| `LocalIpAddress` | `string` | Optional | Terminal Local IP Address |
| `Port` | `int?` | Optional | Terminal Port<br><br>**Default**: `10009`<br><br>**Constraints**: `>= 0`, `<= 65535` |
| `SerialNumber` | `string` | Optional | Terminal Serial Number<br><br>**Constraints**: *Maximum Length*: `24`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `TerminalNumber` | `string` | Optional | Terminal Number<br><br>**Constraints**: *Minimum Length*: `15`, *Maximum Length*: `15` |
| `TerminalTimeouts` | [`TerminalTimeouts1`](../../doc/models/terminal-timeouts-1.md) | Optional | - |
| `TipPercents` | [`TipPercents1`](../../doc/models/tip-percents-1.md) | Optional | - |
| `LocationApiId` | `string` | Optional | Location Api ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `TerminalApiId` | `string` | Optional | Terminal Api ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `HeaderLine1` | `string` | Optional | Header Line 1<br><br>**Constraints**: *Maximum Length*: `32` |
| `HeaderLine2` | `string` | Optional | Header Line 2<br><br>**Constraints**: *Maximum Length*: `32` |
| `HeaderLine3` | `string` | Optional | Header Line 3<br><br>**Constraints**: *Maximum Length*: `32` |
| `HeaderLine4` | `string` | Optional | Header Line 4<br><br>**Constraints**: *Maximum Length*: `32` |
| `HeaderLine5` | `string` | Optional | Header Line 5<br><br>**Constraints**: *Maximum Length*: `32` |
| `TrailerLine1` | `string` | Optional | Trailer Line 1<br><br>**Constraints**: *Maximum Length*: `32` |
| `TrailerLine2` | `string` | Optional | Trailer Line 2<br><br>**Constraints**: *Maximum Length*: `32` |
| `TrailerLine3` | `string` | Optional | Trailer Line 3<br><br>**Constraints**: *Maximum Length*: `32` |
| `TrailerLine4` | `string` | Optional | Trailer Line 4<br><br>**Constraints**: *Maximum Length*: `32` |
| `TrailerLine5` | `string` | Optional | Trailer Line 5<br><br>**Constraints**: *Maximum Length*: `32` |
| `DefaultCheckin` | `string` | Optional | Default Checkin<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `DefaultCheckout` | `string` | Optional | Default Checkout<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `DefaultRoomRate` | `int?` | Optional | Default Room Rate<br><br>**Constraints**: `>= 0`, `<= 100` |
| `DefaultRoomNumber` | `string` | Optional | Default Room Number<br><br>**Constraints**: *Maximum Length*: `12` |
| `Debit` | `bool?` | Optional | Debit |
| `Emv` | `bool?` | Optional | EMV |
| `CashbackEnable` | `bool?` | Optional | Cashback Enable |
| `PrintEnable` | `bool?` | Optional | Print Enable |
| `SigCaptureEnable` | `bool?` | Optional | Sig Capture Enable |
| `IsProvisioned` | `bool?` | Optional | Is Provisioned |
| `TipEnable` | `bool?` | Optional | Tip Enable |
| `ValidatedDecryption` | `bool?` | Optional | Validated Decryption |
| `CommunicationType` | `object` | Optional | - |
| `Active` | `bool?` | Optional | Active |
| `Id` | `string` | Optional | Terminal ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `CreatedTs` | `int?` | Optional | Created Time Stamp |
| `ModifiedTs` | `int?` | Optional | Modified Time Stamp |
| `LastRegistrationTs` | `int?` | Optional | Modified Time Stamp |
| `CreatedUserId` | `string` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ModifiedUserId` | `string` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "default_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "terminal_application_id": "11e95f8ec39de8fbdb0a4f1a",
  "terminal_cvm_id": "11e95f8ec39de8fbdb0a4f1a",
  "title": "My terminal",
  "mac_address": "3D:F2:C9:A6:B3:4F",
  "local_ip_address": "192.168.0.10",
  "port": 10009,
  "serial_number": "1234567890",
  "terminal_number": "973456789012367",
  "header_line_1": "line 1 sample",
  "header_line_2": "line 2 sample",
  "header_line_3": "line 3 sample",
  "header_line_4": "line 4 sample",
  "header_line_5": "line 5 sample",
  "trailer_line_1": "trailer 1 sample",
  "trailer_line_2": "trailer 2 sample",
  "trailer_line_3": "trailer 3 sample",
  "trailer_line_4": "trailer 4 sample",
  "trailer_line_5": "trailer 5 sample",
  "default_checkin": "2021-12-01",
  "default_checkout": "2021-12-01",
  "default_room_rate": 56,
  "default_room_number": "303",
  "debit": false,
  "emv": false,
  "cashback_enable": false,
  "print_enable": false,
  "sig_capture_enable": false,
  "is_provisioned": false,
  "tip_enable": false,
  "validated_decryption": false,
  "active": true,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "last_registration_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "terminal_manufacturer_code": "1",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

