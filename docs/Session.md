# Komoju::Session

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **resource** | **String** |  |  |
| **mode** | [**SessionMode**](SessionMode.md) |  |  |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **session_url** | **String** |  |  |
| **return_url** | **String** |  |  |
| **default_locale** | [**Locale**](Locale.md) |  |  |
| **payment_methods** | [**Array&lt;PaymentMethod&gt;**](PaymentMethod.md) |  |  |
| **created_at** | **String** |  |  |
| **cancelled_at** | **String** |  |  |
| **completed_at** | **String** |  |  |
| **status** | [**SessionStatus**](SessionStatus.md) |  |  |
| **expired** | **Boolean** |  |  |
| **metadata** | **Object** |  |  |
| **payment** | **String** |  |  |
| **payment_data** | [**PaymentData**](PaymentData.md) |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Session.new(
  id: null,
  resource: null,
  mode: null,
  amount: null,
  currency: null,
  session_url: null,
  return_url: null,
  default_locale: null,
  payment_methods: null,
  created_at: null,
  cancelled_at: null,
  completed_at: null,
  status: null,
  expired: null,
  metadata: null,
  payment: null,
  payment_data: null
)
```

