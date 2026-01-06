# Komoju::Payment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **resource** | **String** |  |  |
| **status** | [**PaymentStatus**](PaymentStatus.md) |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **tax** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **customer** | **String** |  |  |
| **payment_deadline** | **String** |  |  |
| **payment_details** | **String** |  |  |
| **payment_method_fee** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **total** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **description** | **String** |  |  |
| **captured_at** | **String** |  |  |
| **external_order_num** | **String** |  |  |
| **metadata** | **Object** |  |  |
| **created_at** | **String** |  |  |
| **amount_refunded** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **locale** | [**Locale**](Locale.md) |  |  |
| **session** | **String** |  |  |
| **customer_family_name** | **String** |  |  |
| **customer_given_name** | **String** |  |  |
| **mcc** | **String** |  |  |
| **statement_descriptor** | **String** |  |  |
| **refunds** | **Array&lt;Object&gt;** |  |  |
| **refund_requests** | **Array&lt;Object&gt;** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Payment.new(
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
  mcc: null,
  statement_descriptor: null,
  refunds: null,
  refund_requests: null
)
```

