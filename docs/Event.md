# Komoju::Event

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **type** | **String** |  |  |
| **resource** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **reason** | **String** |  |  |
| **data** | [**Payment**](Payment.md) |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Event.new(
  id: null,
  type: null,
  resource: null,
  created_at: null,
  reason: null,
  data: null
)
```

