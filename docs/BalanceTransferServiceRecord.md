# Komoju::BalanceTransferServiceRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **recipient** | **String** |  |  |
| **remitter** | **String** |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **happened_at** | **Time** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::BalanceTransferServiceRecord.new(
  type: null,
  recipient: null,
  remitter: null,
  amount: null,
  currency: null,
  happened_at: null
)
```

