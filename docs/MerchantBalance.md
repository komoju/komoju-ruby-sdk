# Komoju::MerchantBalance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  |  |
| **frequency** | [**SettlementFrequency**](SettlementFrequency.md) |  |  |
| **settlement_minimum_amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::MerchantBalance.new(
  currency: null,
  frequency: null,
  settlement_minimum_amount: null
)
```

