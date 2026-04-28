# Komoju::CreatePaymentRequestWithCustomer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | The payment amount before tax, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **capture** | **Boolean** | If &#x60;false&#x60;, the payment will be authorized on success, and you must manually capture it later to secure funds.  The payment will be captured immediately if omitted. | [optional] |
| **description** | **String** | A description from your application for this payment. | [optional] |
| **tax** | [**CreatePaymentRequestWithPaymentDetailsTax**](CreatePaymentRequestWithPaymentDetailsTax.md) |  | [optional] |
| **currency** | [**Currency**](Currency.md) |  |  |
| **external_order_num** | **String** | A unique ID from your application used to track this payment. | [optional] |
| **return_url** | **String** | For offsite payment methods, specify the URL where user will be redirected to after they have completed the payment. | [optional] |
| **cancel_url** | **String** | For offsite payment methods, specify the URL where user will be redirected to if they cancel the payment. | [optional] |
| **locale** | [**Locale**](Locale.md) |  | [optional] |
| **metadata** | **Object** | Specify a key-value map which will be stored on the payment. You can use this field to store metadata related to this payment. Keys and values must be strings. Keys have a maximum length of 30 characters. Values have a maximum length of 2000 characters. | [optional] |
| **mcc** | **String** | On supported merchant and supported payment methods, specify a custom Merchant Category Code (MCC) for this payment.  See [Dynamic Statement Descriptors &amp; MCCs](https://doc.komoju.com/docs/payments-with-dynamic-statement-descriptors) for more information. | [optional] |
| **statement_descriptor** | [**StatementDescriptor**](StatementDescriptor.md) |  | [optional] |
| **fraud_details** | [**FraudDetails**](FraudDetails.md) |  | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |
| **customer** | **String** | For a subscription payment, specify customer&#39;s identifier for this payment.  This identifier can be obtained from [Customer: Create](https://doc.komoju.com/reference/createcustomer) endpoint. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CreatePaymentRequestWithCustomer.new(
  amount: 1000,
  capture: null,
  description: Payment description,
  tax: null,
  currency: null,
  external_order_num: ORDER-12345,
  return_url: https://example.com/order/complete,
  cancel_url: https://example.com/cart,
  locale: null,
  metadata: null,
  mcc: 5799,
  statement_descriptor: null,
  fraud_details: null,
  platform_details: null,
  customer: cust14ur4hvws08idzacf6et8
)
```

