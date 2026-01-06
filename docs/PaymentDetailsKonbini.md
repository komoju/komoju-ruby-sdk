# Komoju::PaymentDetailsKonbini

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **store** | **String** |  |  |
| **email** | **String** |  |  |
| **phone** | **String** |  | [optional] |
| **expiry_days** | **Integer** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsKonbini.new(
  type: null,
  store: null,
  email: null,
  phone: null,
  expiry_days: null
)
```

