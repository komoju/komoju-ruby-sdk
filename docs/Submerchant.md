# Komoju::Submerchant

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submerchant_id** | **String** |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **platform_fee** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Submerchant.new(
  submerchant_id: null,
  amount: null,
  platform_fee: null
)
```

