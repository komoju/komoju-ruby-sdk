# Komoju::Submerchant

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submerchant_id** | **String** | A unique 25-character alphanumeric merchant identifier. |  |
| **amount** | **Integer** | The amount with tax included, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **platform_fee** | **Integer** | The platform fee amount, tax included, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Submerchant.new(
  submerchant_id: submerc1od2nc89s6u5hh6x4g,
  amount: 900,
  platform_fee: 100
)
```

