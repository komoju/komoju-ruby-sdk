# Komoju::CreateDisbursementRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **account_number** | **String** |  |  |
| **account_type** | **String** |  |  |
| **account_name_kana** | **String** |  |  |
| **bank_code** | **String** |  |  |
| **branch_code** | **String** |  |  |
| **external_id** | **String** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CreateDisbursementRequest.new(
  amount: null,
  currency: null,
  account_number: null,
  account_type: null,
  account_name_kana: null,
  bank_code: null,
  branch_code: null,
  external_id: null
)
```

