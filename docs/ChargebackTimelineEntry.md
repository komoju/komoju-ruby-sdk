# Komoju::ChargebackTimelineEntry

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Timeline event type (e.g. \&quot;created\&quot;, \&quot;defended\&quot;, \&quot;response_due\&quot;). |  |
| **occurred_at** | **Time** | When the event occurred. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackTimelineEntry.new(
  type: null,
  occurred_at: null
)
```

