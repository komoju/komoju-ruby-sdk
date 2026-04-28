# Komoju::BalanceTransferServiceRecord

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | The type identifier for this balance transfer record. |  |
| **recipient** | **String** | Identifier of the merchant receiving the funds. |  |
| **remitter** | **String** | Identifier of the merchant sending the funds. |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **happened_at** | **Time** | Timestamp when the balance transfer occurred. |  |

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

