# Komoju::Customer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;customer\&quot;. |  |
| **email** | **String** | Customer&#39;s email address, or null if not provided. |  |
| **source** | [**CustomerSource**](CustomerSource.md) |  |  |
| **metadata** | **Object** | Arbitrary key-value metadata attached to this customer. |  |
| **created_at** | **Time** | Timestamp when the customer was created. |  |
| **locale** | [**Locale**](Locale.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Customer.new(
  id: null,
  resource: null,
  email: null,
  source: null,
  metadata: null,
  created_at: null,
  locale: null
)
```

