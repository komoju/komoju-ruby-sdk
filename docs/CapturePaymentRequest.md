# Komoju::CapturePaymentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | The payment amount before tax, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **tax** | [**CapturePaymentRequestTax**](CapturePaymentRequestTax.md) |  | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CapturePaymentRequest.new(
  amount: 1000,
  tax: null,
  platform_details: null
)
```

