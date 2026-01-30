# Komoju::Transaction

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **type** | **String** |  |  |
| **amount_cents** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **happened_at** | **Time** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Transaction.new(
  id: null,
  type: null,
  amount_cents: null,
  happened_at: null
)
```

