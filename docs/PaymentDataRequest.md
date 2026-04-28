# Komoju::PaymentDataRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **capture** | **String** | Whether to capture the payment automatically on completion, or hold it for manual capture later. | [optional] |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **external_order_num** | **String** | Merchant-assigned order reference number to associate with the payment. | [optional] |
| **name** | **String** | Customer&#39;s full name. | [optional] |
| **name_kana** | **String** | Customer&#39;s full name in katakana. | [optional] |
| **mcc** | **String** | Merchant Category Code to use for this payment. | [optional] |
| **intent** | [**Intent**](Intent.md) |  | [optional] |
| **statement_descriptor** | [**StatementDescriptor**](StatementDescriptor.md) |  | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |
| **billing_address** | [**Address**](Address.md) |  | [optional] |
| **shipping_address** | [**Address**](Address.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PaymentDataRequest.new(
  capture: null,
  amount: null,
  currency: null,
  external_order_num: null,
  name: null,
  name_kana: null,
  mcc: null,
  intent: null,
  statement_descriptor: null,
  platform_details: null,
  billing_address: null,
  shipping_address: null
)
```

