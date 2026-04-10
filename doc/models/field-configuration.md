
# Field Configuration

field_configuration

*This model accepts additional fields of type object.*

## Structure

`FieldConfiguration`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CssMini` | `bool?` | Optional | CSS Mini |
| `Stack` | [`Stack?`](../../doc/models/stack.md) | Optional | - |
| `Header` | [`Header2`](../../doc/models/header-2.md) | Optional | - |
| `Body` | [`Body2`](../../doc/models/body-2.md) | Optional | - |
| `Footer` | [`Footer2`](../../doc/models/footer-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |

## Example (as JSON)

```json
{
  "css_mini": true,
  "stack": "horizontal",
  "header": {
    "settings": {
      "enabled": false,
      "columns": 202.28,
      "rows": 235.78,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "fields": [
      {
        "id": "id8",
        "label": "label8",
        "field_type": "field_type4",
        "position": [
          "position7",
          "position8",
          "position9"
        ],
        "required": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "body": {
    "settings": {
      "enabled": false,
      "columns": 202.28,
      "rows": 235.78,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "fields": [
      {
        "id": "id8",
        "label": "label8",
        "field_type": "field_type4",
        "position": [
          "position7",
          "position8",
          "position9"
        ],
        "required": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "id": "id8",
        "label": "label8",
        "field_type": "field_type4",
        "position": [
          "position7",
          "position8",
          "position9"
        ],
        "required": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "id": "id8",
        "label": "label8",
        "field_type": "field_type4",
        "position": [
          "position7",
          "position8",
          "position9"
        ],
        "required": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "footer": {
    "settings": {
      "enabled": false,
      "columns": 202.28,
      "rows": 235.78,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "fields": [
      {
        "id": "id8",
        "label": "label8",
        "field_type": "field_type4",
        "position": [
          "position7",
          "position8",
          "position9"
        ],
        "required": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "id": "id8",
        "label": "label8",
        "field_type": "field_type4",
        "position": [
          "position7",
          "position8",
          "position9"
        ],
        "required": false,
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

