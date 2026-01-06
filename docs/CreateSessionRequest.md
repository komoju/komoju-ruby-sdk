# Komoju::CreateSessionRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **return_url** | **String** |  | [optional] |
| **mode** | [**SessionMode**](SessionMode.md) |  | [optional] |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **email** | **String** |  | [optional] |
| **expires_in_seconds** | **Integer** | Time in seconds until the session expires after being created. The default value and upper limit are 86,400 seconds (24 hours). | [optional][default to 86400] |
| **external_customer_id** | **String** |  | [optional] |
| **payment_types** | [**Array&lt;PaymentType&gt;**](PaymentType.md) |  | [optional] |
| **default_locale** | [**Locale**](Locale.md) |  | [optional] |
| **line_items** | [**Array&lt;LineItem&gt;**](LineItem.md) |  | [optional] |
| **payment_data** | [**PaymentData**](PaymentData.md) |  | [optional] |
| **customer_id** | **String** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::CreateSessionRequest.new(
  return_url: null,
  mode: null,
  amount: null,
  currency: null,
  email: null,
  expires_in_seconds: null,
  external_customer_id: null,
  payment_types: null,
  default_locale: null,
  line_items: null,
  payment_data: null,
  customer_id: null
)
```

