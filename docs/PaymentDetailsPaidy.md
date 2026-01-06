# Komoju::PaymentDetailsPaidy

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **customer_age** | **Integer** |  | [optional] |
| **customer_last_order_amount** | **Integer** |  | [optional] |
| **customer_last_order_at** | **Integer** |  | [optional] |
| **customer_lifetime_value** | **Integer** |  | [optional] |
| **customer_name** | **String** |  |  |
| **customer_order_count** | **Integer** |  | [optional] |
| **email** | **String** |  | [optional] |
| **phone** | **String** |  | [optional] |
| **external_customer_id** | **String** |  | [optional] |
| **item_title** | **String** |  | [optional] |
| **customer_name_kana** | **String** |  | [optional] |
| **capture** | **Boolean** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsPaidy.new(
  type: null,
  customer_age: null,
  customer_last_order_amount: null,
  customer_last_order_at: null,
  customer_lifetime_value: null,
  customer_name: null,
  customer_order_count: null,
  email: null,
  phone: null,
  external_customer_id: null,
  item_title: null,
  customer_name_kana: null,
  capture: null
)
```

