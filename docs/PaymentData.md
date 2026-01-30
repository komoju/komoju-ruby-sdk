# Komoju::PaymentData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **capture** | **String** |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **external_order_num** | **String** |  |  |
| **name** | **String** |  |  |
| **name_kana** | **String** |  |  |
| **mcc** | **String** |  |  |
| **intent** | [**Intent**](Intent.md) |  |  |
| **statement_descriptor** | [**StatementDescriptor**](StatementDescriptor.md) |  |  |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PaymentData.new(
  capture: null,
  amount: null,
  currency: null,
  external_order_num: null,
  name: null,
  name_kana: null,
  mcc: null,
  intent: null,
  statement_descriptor: null,
  platform_details: null
)
```

