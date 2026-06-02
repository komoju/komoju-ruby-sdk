# Komoju::BarcodePendingResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Barcode generation is pending |  |
| **retry_after** | **Integer** | Request may be retried after specified amount of seconds |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::BarcodePendingResponse.new(
  status: null,
  retry_after: null
)
```

