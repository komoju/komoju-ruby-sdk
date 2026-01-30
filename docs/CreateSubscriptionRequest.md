# Komoju::CreateSubscriptionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **period** | [**SubscriptionPeriod**](SubscriptionPeriod.md) |  |  |
| **metadata** | **Object** | Store any additional data you want to associate with the subscription. The object&#39;s keys and values must be strings. Keys have a maximum length of 30 characters. Values have a maximum length of 2000 characters. | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CreateSubscriptionRequest.new(
  customer: null,
  amount: null,
  currency: null,
  period: null,
  metadata: null
)
```

