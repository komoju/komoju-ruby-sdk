# Komoju::Customer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **resource** | **String** |  |  |
| **email** | **String** |  |  |
| **source** | [**CustomerSource**](CustomerSource.md) |  |  |
| **metadata** | [**CustomerMetadata**](CustomerMetadata.md) |  |  |
| **created_at** | **Time** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Customer.new(
  id: null,
  resource: null,
  email: null,
  source: null,
  metadata: null,
  created_at: null
)
```

