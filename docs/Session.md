# Komoju::Session

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** |  |  |
| **mode** | [**SessionMode**](SessionMode.md) |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **session_url** | **String** |  |  |
| **return_url** | **String** |  |  |
| **default_locale** | [**Locale**](Locale.md) |  |  |
| **payment_methods** | [**Array&lt;PaymentMethod&gt;**](PaymentMethod.md) |  |  |
| **created_at** | **Time** |  |  |
| **cancelled_at** | **Time** |  |  |
| **completed_at** | **Time** |  |  |
| **status** | [**SessionStatus**](SessionStatus.md) |  |  |
| **expired** | **Boolean** |  |  |
| **merchant** | [**MerchantData**](MerchantData.md) |  |  |
| **metadata** | **Object** |  |  |
| **payment** | **String** |  |  |
| **payment_data** | [**PaymentData**](PaymentData.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

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
  merchant: null,
  metadata: null,
  payment: null,
  payment_data: null
)
```

