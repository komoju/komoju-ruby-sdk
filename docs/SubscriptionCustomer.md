# Komoju::SubscriptionCustomer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** |  |  |
| **uuid** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **merchant_id** | **Integer** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **email** | **String** |  |  |
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

