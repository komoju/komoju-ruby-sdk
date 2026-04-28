# Komoju::PaymentMethodInstallmentsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount due for this installment, in the lowest denomination of the currency. |  |
| **pay_at** | **String** | Date when this installment payment is due. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PaymentMethodInstallmentsInner.new(
  amount: null,
  pay_at: null
)
```

