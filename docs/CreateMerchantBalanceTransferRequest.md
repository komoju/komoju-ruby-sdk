# Komoju::CreateMerchantBalanceTransferRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  | [optional] |
| **currency** | [**Currency**](Currency.md) |  |  |
| **to** | **String** |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CreateMerchantBalanceTransferRequest.new(
  merchant_id: null,
  currency: null,
  to: null,
  amount: null
)
```

