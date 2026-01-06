# Komoju::Transaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **type** | **String** |  |  |
| **amount_cents** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **happened_at** | **Time** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Transaction.new(
  id: null,
  type: null,
  amount_cents: null,
  happened_at: null
)
```

