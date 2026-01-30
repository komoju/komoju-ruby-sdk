# Komoju::AvailablePaymentMethod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name_en** | **String** |  |  |
| **name_ja** | **String** |  |  |
| **name_ko** | **String** |  |  |
| **type_slug** | **String** |  |  |
| **currency** | **String** |  |  |
| **subtypes** | **Array&lt;String&gt;** |  | [optional] |
| **secure_token_supported** | **Array&lt;String&gt;** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::AvailablePaymentMethod.new(
  name_en: null,
  name_ja: null,
  name_ko: null,
  type_slug: null,
  currency: null,
  subtypes: null,
  secure_token_supported: null
)
```

