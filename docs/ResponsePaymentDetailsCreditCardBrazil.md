# Komoju::ResponsePaymentDetailsCreditCardBrazil

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. |  |
| **remote_payment_id** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::ResponsePaymentDetailsCreditCardBrazil.new(
  type: null,
  email: komoju@degica.com,
  remote_payment_id: null
)
```

