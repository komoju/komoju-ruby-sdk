# Komoju::StatementDescriptor

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **statement_descriptor** | **String** | Full statement descriptor in Japanese or English. | [optional] |
| **statement_descriptor_alpha** | **String** | Statement descriptor in alphanumeric characters. | [optional] |
| **statement_descriptor_kana** | **String** | Statement descriptor in katakana characters. | [optional] |
| **statement_city** | **String** | Name of the city to be shown on the statement. | [optional] |
| **contact_phone** | **String** | Contact phone number to be shown on the statement. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::StatementDescriptor.new(
  statement_descriptor: 株式会社KOMOJU,
  statement_descriptor_alpha: KOMOJU,
  statement_descriptor_kana: コモジュ,
  statement_city: Tokyo,
  contact_phone: 0312345678
)
```

