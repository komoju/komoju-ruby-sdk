# Komoju::PaymentDetailsBankTransfer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **phone** | **String** |  |  |
| **email** | **String** |  |  |
| **given_name** | **String** |  |  |
| **family_name** | **String** |  |  |
| **given_name_kana** | **String** |  |  |
| **family_name_kana** | **String** |  |  |
| **expiry_days** | **Integer** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsBankTransfer.new(
  type: null,
  phone: null,
  email: null,
  given_name: null,
  family_name: null,
  given_name_kana: null,
  family_name_kana: null,
  expiry_days: null
)
```

