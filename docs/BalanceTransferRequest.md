# Komoju::BalanceTransferRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **to** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::BalanceTransferRequest.new(
  amount: null,
  to: null
)
```

