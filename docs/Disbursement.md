# Komoju::Disbursement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **fee** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **fee_tax** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **status** | [**DisbursementStatus**](DisbursementStatus.md) |  |  |
| **bank_code** | **String** |  |  |
| **branch_code** | **String** |  |  |
| **account_type** | **String** |  |  |
| **account_number** | **String** |  |  |
| **account_name_kana** | **String** |  |  |
| **error** | **String** |  |  |
| **external_id** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **last_updated_at** | **Time** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Disbursement.new(
  id: null,
  currency: null,
  amount: null,
  fee: null,
  fee_tax: null,
  status: null,
  bank_code: null,
  branch_code: null,
  account_type: null,
  account_number: null,
  account_name_kana: null,
  error: null,
  external_id: null,
  created_at: null,
  last_updated_at: null
)
```

