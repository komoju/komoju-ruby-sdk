# Komoju::SubscriptionCustomer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Internal numeric ID of the customer. |  |
| **uuid** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **merchant_id** | **Integer** | Internal numeric ID of the merchant. |  |
| **created_at** | **Time** | Timestamp when the customer was created. |  |
| **updated_at** | **Time** | Timestamp when the customer was last updated. |  |
| **email** | **String** | Customer&#39;s email address. |  |
| **currency** | [**Currency**](Currency.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SubscriptionCustomer.new(
  id: null,
  uuid: null,
  merchant_id: null,
  created_at: null,
  updated_at: null,
  email: null,
  currency: null
)
```

