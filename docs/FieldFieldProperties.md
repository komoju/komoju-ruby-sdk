# Komoju::FieldFieldProperties

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **external_links** | **Array&lt;String&gt;** | Array of URLs to external resources relevant to this field. | [optional] |
| **min_length** | **Integer** | Minimum character length for the field value. | [optional] |
| **format** | **String** | Semantic format hint for the field value (e.g. \&quot;date\&quot;, \&quot;email\&quot;). | [optional] |
| **pattern** | **String** | Regular expression the field value must match. | [optional] |
| **minimum** | **Integer** | Minimum numeric value for integer fields. | [optional] |
| **maximum** | **Integer** | Maximum numeric value for integer fields. | [optional] |
| **enum** | **Object** | Map of human-readable labels to enum codes for dropdown/radio fields. | [optional] |
| **items** | **Object** | Schema describing each item in an array field. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::FieldFieldProperties.new(
  external_links: null,
  min_length: null,
  format: null,
  pattern: null,
  minimum: null,
  maximum: null,
  enum: null,
  items: null
)
```

