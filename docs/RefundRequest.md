# Komoju::RefundRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric refund request identifier. |  |
| **payment** | **String** | A unique 25-character alphanumeric payment identifier. |  |
| **customer_name** | **String** | Customer&#39;s name in half-width katakana characters. |  |
| **bank_name** | **String** | The name of the bank that customer would like money to be deposited to. |  |
| **bank_code** | **String** | 4-digit bank code. May be &#x60;null&#x60; if it&#39;s not given. |  |
| **branch_name** | **String** | The name of the branch. |  |
| **branch_number** | **String** | 3-digit branch number. |  |
| **account_number** | **String** | 7-digit account number. |  |
| **description** | **String** | Optional description or reason for this refund request. | [optional] |
| **status** | [**RefundRequestStatus**](RefundRequestStatus.md) |  |  |
| **created_at** | **Time** | Timestamp when the refund request was created. |  |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::RefundRequest.new(
  id: refreqlv6wny1ew1a1aq4zum1,
  payment: pay3fj6nnhvws08idzacf6et8,
  customer_name: ｻｲﾄｳ ﾏｻﾋﾛ,
  bank_name: サンプル銀行,
  bank_code: 0900,
  branch_name: 本店,
  branch_number: 100,
  account_number: 1234567,
  description: null,
  status: null,
  created_at: null,
  platform_details: null
)
```

