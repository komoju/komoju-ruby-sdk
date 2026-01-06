# Komoju::CreatePaymentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **capture** | **Boolean** | If false, the payment will be authorized but not be captured. This option is ignored if a payment type is not credit_card. | [optional] |
| **description** | **String** | Plaintext description for annotating a resource. | [optional] |
| **tax** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **currency** | [**Currency**](Currency.md) |  |  |
| **external_order_num** | **String** | A unique ID from your application used to track this payment. | [optional] |
| **return_url** | **String** |  | [optional] |
| **cancel_url** | **String** |  | [optional] |
| **locale** | [**Locale**](Locale.md) |  | [optional] |
| **partner_origin** | **String** |  | [optional] |
| **metadata** | **String** |  | [optional] |
| **payment_details** | [**PaymentDetailsAll**](PaymentDetailsAll.md) |  | [optional] |
| **mcc** | **String** |  | [optional] |
| **statement_descriptor** | [**StatementDescriptor**](StatementDescriptor.md) |  | [optional] |
| **platform_details** | [**PlatformDetails**](PlatformDetails.md) |  | [optional] |
| **customer** | **String** | The ID of an existing customer in which to provide payment details for the payment. This or payment_details must be present. | [optional] |
| **fraud_details** | [**FraudDetails**](FraudDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CreatePaymentRequest.new(
  amount: null,
  capture: null,
  description: null,
  tax: null,
  currency: null,
  external_order_num: null,
  return_url: null,
  cancel_url: null,
  locale: null,
  partner_origin: null,
  metadata: null,
  payment_details: null,
  mcc: null,
  statement_descriptor: null,
  platform_details: null,
  customer: null,
  fraud_details: null
)
```

