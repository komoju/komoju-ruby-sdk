# Komoju::ResponsePaymentDetailsCreditCardBrazil

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. |  |
| **remote_payment_id** | **String** | Remote payment identifier returned by the Brazilian payment gateway. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ResponsePaymentDetailsCreditCardBrazil.new(
  type: null,
  email: example@komoju.com,
  remote_payment_id: null
)
```

