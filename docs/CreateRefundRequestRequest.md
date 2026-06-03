# Komoju::CreateRefundRequestRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | The payment amount before tax, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **customer_name** | **String** | Customer&#39;s name in half-width katakana, as registered at the bank. |  |
| **bank_name** | **String** | Name of the customer&#39;s bank. |  |
| **bank_code** | **String** | Optional 4-digit Zengin bank code. | [optional] |
| **branch_name** | **String** | Name of the customer&#39;s bank branch. | [optional] |
| **branch_number** | **String** | 3-digit branch number. |  |
| **account_type** | **String** | Type of the customer&#39;s bank account. |  |
| **account_number** | **Integer** | 7-digit bank account number to deposit the refund into. |  |
| **include_payment_method_fee** | **Boolean** | Whether the refund should include the original payment method fee. |  |
| **description** | **String** | Optional description or reason for this refund request. | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::CreateRefundRequestRequest.new(
  amount: 1000,
  customer_name: null,
  bank_name: null,
  bank_code: null,
  branch_name: null,
  branch_number: null,
  account_type: null,
  account_number: null,
  include_payment_method_fee: null,
  description: null,
  platform_details: null
)
```

