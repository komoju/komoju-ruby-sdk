# Komoju::PaySessionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **capture** | **String** | Default: auto | [optional] |
| **payment_details** | [**PaymentDetailsAll**](PaymentDetailsAll.md) |  |  |
| **fraud_details** | [**FraudDetails**](FraudDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaySessionRequest.new(
  capture: null,
  payment_details: null,
  fraud_details: null
)
```

