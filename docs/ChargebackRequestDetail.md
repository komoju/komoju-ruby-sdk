# Komoju::ChargebackRequestDetail

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **status** | [**ChargebackStatus**](ChargebackStatus.md) |  |  |
| **reason_code** | **String** | Machine-readable reason code. Internal codes (e.g. \&quot;CB_Fraud\&quot;) are used by default; for Worldpay Visa/Mastercard payments the network&#39;s own reason codes are used instead (e.g. \&quot;10.4\&quot; or \&quot;4837\&quot;). |  |
| **reason** | **String** | Human-readable chargeback reason corresponding to the reason code. |  |
| **created_at** | **Time** | Timestamp when the chargeback was created. |  |
| **due_date** | **Time** | Deadline by which the merchant must respond. |  |
| **last_updated_at** | **Time** | Timestamp when the chargeback was last updated. |  |
| **timeline** | [**Array&lt;ChargebackTimelineEntry&gt;**](ChargebackTimelineEntry.md) | Chronological list of chargeback events. |  |
| **payment** | [**ChargebackPayment**](ChargebackPayment.md) |  |  |
| **customer** | [**ChargebackCustomer**](ChargebackCustomer.md) |  |  |
| **defense** | [**ChargebackDefense**](ChargebackDefense.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackRequestDetail.new(
  id: null,
  status: null,
  reason_code: CB_Fraud,
  reason: null,
  created_at: null,
  due_date: null,
  last_updated_at: null,
  timeline: null,
  payment: null,
  customer: null,
  defense: null
)
```

