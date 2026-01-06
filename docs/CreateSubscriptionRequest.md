# Komoju::CreateSubscriptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer** | **String** |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **period** | [**SubscriptionPeriod**](SubscriptionPeriod.md) |  |  |
| **metadata** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CreateSubscriptionRequest.new(
  customer: null,
  amount: null,
  currency: null,
  period: null,
  metadata: null
)
```

