# Komoju::Payment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric payment identifier. |  |
| **resource** | **String** | Resource name. Will always be &#x60;payment&#x60;. |  |
| **status** | [**PaymentStatus**](PaymentStatus.md) |  |  |
| **amount** | **Integer** | The payment amount before tax, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **tax** | **Integer** | The tax amount, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **customer** | **String** |  |  |
| **payment_deadline** | **String** |  |  |
| **payment_details** | [**ResponsePaymentDetailsAll**](ResponsePaymentDetailsAll.md) |  |  |
| **payment_method_fee** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **description** | **String** | A description for this payment. May be null if it&#39;s not set. |  |
| **captured_at** | **Time** |  |  |
| **external_order_num** | **String** |  |  |
| **metadata** | **Object** |  |  |
| **created_at** | **Time** |  |  |
| **amount_refunded** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **locale** | [**Locale**](Locale.md) |  |  |
| **session** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **customer_family_name** | **String** |  |  |
| **customer_given_name** | **String** |  |  |
| **mcc** | **String** |  |  |
| **statement_descriptor** | **String** |  |  |
| **refunds** | [**Array&lt;Refund&gt;**](Refund.md) | An array of refunds. Will be an empty array if there are no refunds. |  |
| **refund_requests** | [**Array&lt;RefundRequest&gt;**](RefundRequest.md) | An array of refund requests. Will be an empty array if there are no refund requests. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Payment.new(
  id: pay3fj6nnhvws08idzacf6et8,
  resource: null,
  status: null,
  amount: 1000,
  tax: 0,
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

