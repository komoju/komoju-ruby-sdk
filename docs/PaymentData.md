# Komoju::PaymentData

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **capture** | **String** | Whether the payment is captured automatically on completion, or held for manual capture. |  |
| **external_order_num** | **String** | Merchant-assigned order reference number associated with this payment. | [optional] |
| **name** | **String** | Customer&#39;s full name as provided at session creation. | [optional] |
| **name_kana** | **String** | Customer&#39;s full name in katakana as provided at session creation. | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaymentData.new(
  capture: null,
  external_order_num: null,
  name: null,
  name_kana: null,
  platform_details: null
)
```

