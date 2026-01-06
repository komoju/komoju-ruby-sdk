# Komoju::PaymentDetailsCreditCard

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **email** | **String** |  | [optional] |
| **number** | **String** |  |  |
| **month** | **Integer** |  |  |
| **year** | **Integer** |  |  |
| **verification_value** | **String** |  | [optional] |
| **given_name** | **String** |  | [optional] |
| **family_name** | **String** |  | [optional] |
| **name** | **String** |  | [optional] |
| **three_d_secure** | **Boolean** |  | [optional] |
| **expiry_days** | **Integer** |  | [optional] |
| **intent** | [**Intent**](Intent.md) |  | [optional] |
| **initiator** | **String** |  | [optional] |
| **usage** | **String** |  | [optional] |
| **scheme_reference** | **String** | Used for some Visa and Mastercard payments to track the chain of multiple related transactions. Using this field can reduce declines. | [optional] |
| **social_id** | **String** |  | [optional] |
| **first_two_digits_of_pin** | **String** |  | [optional] |
| **corporate_card** | **Boolean** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsCreditCard.new(
  type: null,
  email: null,
  number: null,
  month: null,
  year: null,
  verification_value: null,
  given_name: null,
  family_name: null,
  name: null,
  three_d_secure: null,
  expiry_days: null,
  intent: null,
  initiator: null,
  usage: null,
  scheme_reference: null,
  social_id: null,
  first_two_digits_of_pin: null,
  corporate_card: null
)
```

