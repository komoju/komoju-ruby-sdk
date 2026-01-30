# Komoju::CreateDisbursementRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **account_number** | **String** |  |  |
| **account_type** | **String** |  |  |
| **account_name_kana** | **String** |  |  |
| **bank_code** | **String** |  |  |
| **branch_code** | **String** |  |  |
| **external_id** | **String** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

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

