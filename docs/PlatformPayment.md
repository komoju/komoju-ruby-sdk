# Komoju::PlatformPayment

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;payment\&quot;. |  |
| **status** | [**PaymentStatus**](PaymentStatus.md) |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **tax** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **customer** | **String** | Customer UUID if associated with a customer, otherwise null. |  |
| **payment_deadline** | **String** | Deadline by which the payment must be completed, or null. |  |
| **payment_details** | **String** | Serialized payment method details for this payment. |  |
| **payment_method_fee** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **description** | **String** | Optional description for the payment. |  |
| **captured_at** | **Time** | Timestamp when the payment was captured, or null if not yet captured. |  |
| **external_order_num** | **String** | External order reference from the merchant&#39;s system. |  |
| **metadata** | **Object** | Arbitrary key-value metadata attached to the payment. |  |
| **created_at** | **Time** | Timestamp when the payment was created. |  |
| **amount_refunded** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **locale** | [**Locale**](Locale.md) |  |  |
| **session** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **customer_family_name** | **String** | Customer&#39;s family name. |  |
| **customer_given_name** | **String** | Customer&#39;s given name. |  |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  |  |
| **mcc** | **String** | Merchant Category Code used for this payment. |  |
| **statement_descriptor** | **String** | Statement descriptor shown to the customer on their bank statement. |  |
| **refunds** | **Array&lt;Object&gt;** | Array of refund objects associated with this payment. |  |
| **refund_requests** | **Array&lt;Object&gt;** | Array of refund request objects associated with this payment. |  |

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

