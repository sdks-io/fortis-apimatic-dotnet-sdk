
# Addon

*This model accepts additional fields of type object.*

## Structure

`Addon`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Title` | `string` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `24` |
| `Secret` | `string` | Optional | Secret<br><br>**Constraints**: *Maximum Length*: `36` |
| `IframeUrl` | `string` | Optional | Iframe URL<br><br>**Constraints**: *Maximum Length*: `512` |
| `LocationSetupUrl` | `string` | Optional | Location Setup URL<br><br>**Constraints**: *Maximum Length*: `512` |
| `UserSetupUrl` | `string` | Optional | User Setup URL<br><br>**Constraints**: *Maximum Length*: `512` |
| `EncryptUrlParams` | `bool?` | Optional | Encrypt URL Params |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "encrypt_url_params": true,
  "title": "title4",
  "secret": "secret4",
  "iframe_url": "iframe_url4",
  "location_setup_url": "location_setup_url0",
  "user_setup_url": "user_setup_url6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

