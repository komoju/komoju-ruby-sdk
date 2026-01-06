# Komoju::Transfer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **recipient** | **String** |  |  |
| **remitter** | **String** |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **happened_at** | **Time** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Transfer.new(
  type: null,
  recipient: null,
  remitter: null,
  amount: null,
  currency: null,
  happened_at: null
)
```

