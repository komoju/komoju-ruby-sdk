# Komoju::PaymentMethodApplicationWithSubmittedFields

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **status** | [**PaymentMethodApplicationStatus**](PaymentMethodApplicationStatus.md) |  |  |
| **payments_enabled** | **Boolean** | Whether payments have been enabled following payment-method review. |  |
| **payouts_enabled** | **Boolean** | Whether payouts have been enabled following payment-method review. |  |
| **requested_fields** | [**Array&lt;Field&gt;**](Field.md) | Fields currently required to be submitted for this payment method. |  |
| **newly_requested_fields** | [**Array&lt;Field&gt;**](Field.md) | Fields newly added to the required list since last submission. |  |
| **errored_fields** | [**Array&lt;ErroredField&gt;**](ErroredField.md) | Fields that were submitted but failed validation. |  |
| **submitted_fields** | [**Array&lt;SubmittedField&gt;**](SubmittedField.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaymentMethodApplicationWithSubmittedFields.new(
  merchant_id: null,
  status: null,
  payments_enabled: null,
  payouts_enabled: null,
  requested_fields: null,
  newly_requested_fields: null,
  errored_fields: null,
  submitted_fields: null
)
```

