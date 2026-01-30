# Komoju::SerializedSubmerchantActivePaymentMethodsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **type** | **String** |  |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **percentage** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **fixed_amount_cents** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **minimum_processing_fee_amount_cents** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SerializedSubmerchantActivePaymentMethodsInner.new(
  name: null,
  type: null,
  currency: null,
  percentage: null,
  fixed_amount_cents: null,
  minimum_processing_fee_amount_cents: null
)
```

