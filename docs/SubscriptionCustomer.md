# Komoju::SubscriptionCustomer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **Integer** | Internal numeric ID of the customer. |  |
| **uuid** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **merchant_id** | **Integer** | Internal numeric ID of the merchant. |  |
| **created_at** | **Time** | Timestamp when the customer was created. |  |
| **updated_at** | **Time** | Timestamp when the customer was last updated. |  |
| **email** | **String** | Customer&#39;s email address, or null if not provided. |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **locale** | [**Locale**](Locale.md) |  |  |
| **name** | **String** | Customer-defined display name, or null if not set. |  |
| **phone** | **String** | Customer&#39;s phone number, or null if not set. |  |
| **archived_at** | **Time** | Timestamp when the customer was archived, or null if still active. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SubscriptionCustomer.new(
  id: null,
  uuid: null,
  merchant_id: null,
  created_at: null,
  updated_at: null,
  email: null,
  currency: null,
  locale: null,
  name: null,
  phone: null,
  archived_at: null
)
```

