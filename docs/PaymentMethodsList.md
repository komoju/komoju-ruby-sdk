# Komoju::PaymentMethodsList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submitted_payment_methods** | [**Array&lt;PaymentMethodStatus&gt;**](PaymentMethodStatus.md) | Array of payment methods that have been submitted for review, with their statuses. |  |
| **unsubmitted_payment_methods** | **Array&lt;String&gt;** | Array of payment method type slugs that have not yet been submitted for review. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaymentMethodsList.new(
  submitted_payment_methods: null,
  unsubmitted_payment_methods: null
)
```

