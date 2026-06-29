# Komoju::ChargebackPayment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **created_at** | **Time** | Timestamp when the payment was created. |  |
| **captured_at** | **Time** | Timestamp when the payment was captured, or null. |  |
| **payment_method** | [**ChargebackPaymentMethod**](ChargebackPaymentMethod.md) |  |  |
| **masked_card_number** | **String** | Masked card number, or null if not applicable. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackPayment.new(
  id: null,
  amount: null,
  currency: null,
  created_at: null,
  captured_at: null,
  payment_method: null,
  masked_card_number: null
)
```

