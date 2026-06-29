# Komoju::Event

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **type** | **String** | Event type slug (e.g. \&quot;payment.captured\&quot;, \&quot;payment.expired\&quot;). |  |
| **resource** | **String** | Resource type name, always \&quot;event\&quot;. |  |
| **created_at** | **Time** | Timestamp when this event was created. |  |
| **reason** | **String** | Human-readable reason or description for this event, or null. |  |
| **data** | [**Payment**](Payment.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Event.new(
  id: null,
  type: null,
  resource: null,
  created_at: null,
  reason: null,
  data: null
)
```

