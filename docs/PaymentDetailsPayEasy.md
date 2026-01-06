# Komoju::PaymentDetailsPayEasy

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **email** | **String** |  |  |
| **given_name** | **String** |  |  |
| **family_name** | **String** |  |  |
| **given_name_kana** | **String** |  |  |
| **family_name_kana** | **String** |  |  |
| **phone** | **String** |  |  |
| **expiry_days** | **Integer** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsPayEasy.new(
  type: null,
  email: null,
  given_name: null,
  family_name: null,
  given_name_kana: null,
  family_name_kana: null,
  phone: null,
  expiry_days: null
)
```

