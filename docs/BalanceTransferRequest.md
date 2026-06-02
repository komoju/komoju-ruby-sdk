# Komoju::BalanceTransferRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **to** | **String** |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::BalanceTransferRequest.new(
  amount: null,
  to: null
)
```

