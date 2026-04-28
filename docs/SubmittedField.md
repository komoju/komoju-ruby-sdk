# Komoju::SubmittedField

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **field_type** | **String** | The input type for this field (e.g. \&quot;text\&quot;, \&quot;file\&quot;, \&quot;boolean\&quot;). |  |
| **field** | **String** | Machine-readable key name of the field. |  |
| **field_name** | **String** | Human-readable display name of the field. |  |
| **field_properties** | [**FieldFieldProperties**](FieldFieldProperties.md) |  |  |
| **position** | **Integer** | Display order position of this field in the application form. |  |
| **optional** | **Boolean** | Whether this field is optional (true) or required (false). |  |
| **value** | [**SubmittedFieldAllOfValue**](SubmittedFieldAllOfValue.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SubmittedField.new(
  field_type: null,
  field: null,
  field_name: null,
  field_properties: null,
  position: null,
  optional: null,
  value: null
)
```

