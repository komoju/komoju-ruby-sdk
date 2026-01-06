# Komoju::Subscription

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **resource** | **String** |  |  |
| **status** | **String** |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **customer** | [**SubscriptionCustomer**](SubscriptionCustomer.md) |  |  |
| **period** | [**SubscriptionPeriod**](SubscriptionPeriod.md) |  |  |
| **day** | **Integer** |  |  |
| **payment_details** | [**SubscriptionPaymentDetails**](SubscriptionPaymentDetails.md) |  |  |
| **retry_count** | **Integer** |  |  |
| **retry_at** | **Time** |  |  |
| **next_capture_at** | **Time** |  |  |
| **created_at** | **Time** |  |  |
| **ended_at** | **Time** |  |  |
| **metadata** | **String** |  |  |
| **payments** | **Array&lt;Object&gt;** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

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

