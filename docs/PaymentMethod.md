# Komoju::PaymentMethod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **hashed_gateway** | **String** |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **exchange_rate** | **Float** |  |  |
| **offsite** | **Boolean** |  | [optional] |
| **additional_fields** | **Array&lt;String&gt;** |  | [optional] |
| **brands** | [**PaymentMethodBrands**](PaymentMethodBrands.md) |  | [optional] |
| **seven_eleven_merchant_number** | **String** | Only for Konbini | [optional] |
| **installments** | [**Array&lt;PaymentMethodInstallmentsInner&gt;**](PaymentMethodInstallmentsInner.md) | Only for Komoju Pay | [optional] |
| **api_endpoint** | **String** | Only for Komoju Pay | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

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

