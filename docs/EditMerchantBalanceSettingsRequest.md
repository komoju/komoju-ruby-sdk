# Komoju::EditMerchantBalanceSettingsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  | [optional] |
| **currency** | [**Currency**](Currency.md) |  |  |
| **frequency** | [**SettlementFrequency**](SettlementFrequency.md) |  |  |
| **settlement_minimum_amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::EditMerchantBalanceSettingsRequest.new(
  merchant_id: null,
  currency: null,
  frequency: null,
  settlement_minimum_amount: null
)
```

