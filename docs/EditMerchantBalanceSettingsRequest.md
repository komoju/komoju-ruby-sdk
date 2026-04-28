# Komoju::EditMerchantBalanceSettingsRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** | A unique 25-character alphanumeric resource identifier. | [optional] |
| **currency** | [**Currency**](Currency.md) |  |  |
| **frequency** | [**SettlementFrequency**](SettlementFrequency.md) |  |  |
| **settlement_minimum_amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::EditMerchantBalanceSettingsRequest.new(
  merchant_id: null,
  currency: null,
  frequency: null,
  settlement_minimum_amount: null
)
```

