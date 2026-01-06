# Komoju::CapturePaymentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **tax** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CapturePaymentRequest.new(
  amount: null,
  tax: null,
  platform_details: null
)
```

