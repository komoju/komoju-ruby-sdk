# Komoju::PaymentDetailsCreditCardBrazil

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **email** | **String** |  |  |
| **number** | **String** |  |  |
| **month** | **Integer** |  |  |
| **year** | **Integer** |  |  |
| **verification_value** | **String** |  |  |
| **name** | **String** |  |  |
| **cpf_or_cnpj** | **String** |  |  |
| **customer_ip** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsCreditCardBrazil.new(
  type: null,
  email: null,
  number: null,
  month: null,
  year: null,
  verification_value: null,
  name: null,
  cpf_or_cnpj: null,
  customer_ip: null
)
```

