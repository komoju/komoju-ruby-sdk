# Komoju::PaymentMethodStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | [**PaymentMethodApplicationStatus**](PaymentMethodApplicationStatus.md) |  |  |
| **payment_method** | **String** | The type slug of the payment method this status applies to. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaymentMethodStatus.new(
  status: null,
  payment_method: null
)
```

