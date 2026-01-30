# Komoju::PaymentMethodsList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submitted_payment_methods** | [**Array&lt;PaymentMethodStatus&gt;**](PaymentMethodStatus.md) |  |  |
| **unsubmitted_payment_methods** | **Array&lt;String&gt;** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PaymentMethodsList.new(
  submitted_payment_methods: null,
  unsubmitted_payment_methods: null
)
```

