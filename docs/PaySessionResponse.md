# Komoju::PaySessionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **redirect_url** | **String** | URL to redirect the customer to after submitting payment details, or null if no redirect is required. |  |
| **status** | [**SessionStatus**](SessionStatus.md) |  |  |
| **payment** | [**Payment**](Payment.md) |  |  |
| **app_url** | **String** | URL for the payment app, if applicable. | [optional] |
| **customer** | [**PaySessionResponseCustomer**](PaySessionResponseCustomer.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PaySessionResponse.new(
  redirect_url: null,
  status: null,
  payment: null,
  app_url: null,
  customer: null
)
```

