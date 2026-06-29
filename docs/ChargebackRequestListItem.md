# Komoju::ChargebackRequestListItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **payment_id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **payment_method** | [**ChargebackPaymentMethod**](ChargebackPaymentMethod.md) |  |  |
| **reason_code** | **String** | Machine-readable reason code. Internal codes (e.g. \&quot;CB_Fraud\&quot;) are used by default; for Worldpay Visa/Mastercard payments the network&#39;s own reason codes are used instead (e.g. \&quot;10.4\&quot; or \&quot;4837\&quot;). |  |
| **reason** | **String** | Human-readable chargeback reason corresponding to the reason code. |  |
| **created_at** | **Time** | Timestamp when the chargeback was created. |  |
| **due_date** | **Time** | Deadline by which the merchant must respond. |  |
| **status** | [**ChargebackStatus**](ChargebackStatus.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackRequestListItem.new(
  id: null,
  payment_id: null,
  amount: null,
  currency: null,
  payment_method: null,
  reason_code: CB_Fraud,
  reason: null,
  created_at: null,
  due_date: null,
  status: null
)
```

