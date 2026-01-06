# Komoju::PaymentDetailsCreditCardKorea

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **number** | **String** |  |  |
| **month** | **Integer** |  |  |
| **year** | **Integer** |  |  |
| **verification_value** | **String** |  | [optional] |
| **social_id** | **String** |  | [optional] |
| **first_two_digits_of_pin** | **String** |  |  |
| **corporate_card** | **Boolean** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsCreditCardKorea.new(
  type: null,
  number: null,
  month: null,
  year: null,
  verification_value: null,
  social_id: null,
  first_two_digits_of_pin: null,
  corporate_card: null
)
```

