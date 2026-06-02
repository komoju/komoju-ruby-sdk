# Komoju::CreateDisbursementRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **account_number** | **String** | Recipient&#39;s bank account number. |  |
| **account_type** | **String** | Type of the recipient&#39;s bank account. |  |
| **account_name_kana** | **String** | Name of the recipient bank account holder in katakana. |  |
| **bank_code** | **String** | 4-digit Zengin bank code. |  |
| **branch_code** | **String** | 3-digit Zengin branch code. |  |
| **external_id** | **String** | Merchant-assigned external reference ID for this disbursement. | [optional] |

## Example

```ruby
require 'komoju-sdk'

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

