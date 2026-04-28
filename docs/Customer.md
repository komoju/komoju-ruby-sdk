# Komoju::Customer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;customer\&quot;. |  |
| **email** | **String** | Customer&#39;s email address. |  |
| **source** | [**CustomerSource**](CustomerSource.md) |  |  |
| **metadata** | [**CustomerMetadata**](CustomerMetadata.md) |  |  |
| **created_at** | **Time** | Timestamp when the customer was created. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Customer.new(
  id: null,
  resource: null,
  email: null,
  source: null,
  metadata: null,
  created_at: null
)
```

