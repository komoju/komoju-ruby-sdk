# Komoju::PlatformPayment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** |  |  |
| **status** | [**PaymentStatus**](PaymentStatus.md) |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **tax** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **customer** | **String** |  |  |
| **payment_deadline** | **String** |  |  |
| **payment_details** | **String** |  |  |
| **payment_method_fee** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **description** | **String** |  |  |
| **captured_at** | **Time** |  |  |
| **external_order_num** | **String** |  |  |
| **metadata** | **Object** |  |  |
| **created_at** | **Time** |  |  |
| **amount_refunded** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **locale** | [**Locale**](Locale.md) |  |  |
| **session** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **customer_family_name** | **String** |  |  |
| **customer_given_name** | **String** |  |  |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  |  |
| **mcc** | **String** |  |  |
| **statement_descriptor** | **String** |  |  |
| **refunds** | **Array&lt;Object&gt;** |  |  |
| **refund_requests** | **Array&lt;Object&gt;** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PlatformPayment.new(
  id: null,
  resource: null,
  status: null,
  amount: null,
  tax: null,
  customer: null,
  payment_deadline: null,
  payment_details: null,
  payment_method_fee: null,
  total: null,
  currency: null,
  description: null,
  captured_at: null,
  external_order_num: null,
  metadata: null,
  created_at: null,
  amount_refunded: null,
  locale: null,
  session: null,
  customer_family_name: null,
  customer_given_name: null,
  platform_details: null,
  mcc: null,
  statement_descriptor: null,
  refunds: null,
  refund_requests: null
)
```

