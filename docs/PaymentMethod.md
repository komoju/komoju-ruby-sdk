# Komoju::PaymentMethod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Machine-readable type slug for this payment method (e.g. \&quot;credit_card\&quot;, \&quot;konbini\&quot;). |  |
| **hashed_gateway** | **String** | Hashed identifier of the payment gateway processing this method. | [optional] |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **currency** | [**Currency**](Currency.md) |  | [optional] |
| **exchange_rate** | **Float** | Exchange rate applied when this payment method&#39;s currency differs from the session currency. | [optional] |
| **offsite** | **Boolean** | Whether this payment method redirects the customer to an external site to complete payment. | [optional] |
| **additional_fields** | **Array&lt;String&gt;** | Names of additional input fields required to complete payment with this method. | [optional] |
| **brands** | [**PaymentMethodBrands**](PaymentMethodBrands.md) |  | [optional] |
| **seven_eleven_merchant_number** | **String** | Only for Konbini | [optional] |
| **installments** | [**Array&lt;PaymentMethodInstallmentsInner&gt;**](PaymentMethodInstallmentsInner.md) | Only for Komoju Pay | [optional] |
| **api_endpoint** | **String** | Only for Komoju Pay | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaymentMethod.new(
  type: null,
  hashed_gateway: null,
  amount: null,
  currency: null,
  exchange_rate: null,
  offsite: null,
  additional_fields: null,
  brands: null,
  seven_eleven_merchant_number: null,
  installments: null,
  api_endpoint: null
)
```

