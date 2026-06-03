# Komoju::Balance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  |  |
| **total_balance_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Balance.new(
  currency: null,
  total_balance_cents: null
)
```

