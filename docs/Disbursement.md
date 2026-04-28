# Komoju::Disbursement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **fee** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **fee_tax** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **status** | [**DisbursementStatus**](DisbursementStatus.md) |  |  |
| **bank_code** | **String** | 4-digit Zengin bank code of the recipient&#39;s bank. |  |
| **branch_code** | **String** | 3-digit Zengin branch code. |  |
| **account_type** | **String** | Type of the recipient&#39;s bank account. |  |
| **account_number** | **String** | Recipient&#39;s bank account number. |  |
| **account_name_kana** | **String** | Name of the recipient bank account holder in katakana. |  |
| **error** | **String** | Error message if the disbursement failed, otherwise null. |  |
| **external_id** | **String** | Merchant-assigned external reference ID for this disbursement. |  |
| **created_at** | **Time** | Timestamp when the disbursement was created. |  |
| **last_updated_at** | **Time** | Timestamp when the disbursement record was last updated. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

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

