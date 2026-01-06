# Komoju::RefundPaymentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **description** | **String** |  | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::RefundPaymentRequest.new(
  amount: null,
  description: null,
  platform_details: null
)
```

