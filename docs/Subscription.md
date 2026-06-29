# Komoju::Subscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;subscription\&quot;. |  |
| **status** | **String** | Current status of the subscription (e.g. \&quot;active\&quot;, \&quot;cancelled\&quot;). |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **customer** | [**SubscriptionCustomer**](SubscriptionCustomer.md) |  |  |
| **period** | [**SubscriptionPeriod**](SubscriptionPeriod.md) |  |  |
| **day** | **Integer** | Day of the period on which the subscription is charged. |  |
| **payment_details** | [**SubscriptionPaymentDetails**](SubscriptionPaymentDetails.md) |  |  |
| **retry_count** | **Integer** | Number of times payment has been retried after failure. |  |
| **retry_at** | **Time** | Timestamp of the next scheduled payment retry, or null. |  |
| **next_capture_at** | **Time** | Timestamp of the next scheduled subscription charge. |  |
| **created_at** | **Time** | Timestamp when the subscription was created. |  |
| **ended_at** | **Time** | Timestamp when the subscription ended, or null if still active. |  |
| **metadata** | **Object** | Arbitrary key-value metadata attached to the subscription. |  |
| **payments** | **Array&lt;String&gt;** | Array of payment UUIDs associated with this subscription. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Subscription.new(
  id: null,
  resource: null,
  status: null,
  amount: null,
  currency: null,
  customer: null,
  period: null,
  day: null,
  payment_details: null,
  retry_count: null,
  retry_at: null,
  next_capture_at: null,
  created_at: null,
  ended_at: null,
  metadata: null,
  payments: null
)
```

