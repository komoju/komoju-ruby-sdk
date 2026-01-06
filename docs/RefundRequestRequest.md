# Komoju::RefundRequestRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **customer_name** | **String** |  |  |
| **bank_name** | **String** |  |  |
| **bank_code** | **String** |  | [optional] |
| **branch_name** | **String** |  | [optional] |
| **branch_number** | **String** |  |  |
| **account_type** | **String** |  |  |
| **account_number** | **Integer** |  |  |
| **include_payment_method_fee** | **Boolean** |  |  |
| **description** | **String** |  | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::RefundRequestRequest.new(
  amount: null,
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

