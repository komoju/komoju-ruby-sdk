# Komoju::Address

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** | Address name. | [optional] |
| **street_address1** | **String** | Address line 1. | [optional] |
| **street_address2** | **String** | Address line 2. | [optional] |
| **city** | **String** | Address city. | [optional] |
| **state** | **String** | Address state. | [optional] |
| **zipcode** | **String** | Address ZIP code. | [optional] |
| **country** | **String** | Address country. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Address.new(
  name: Taro Tanaka,
  street_address1: 5-2-1 Ginza,
  street_address2: 3rd floor,
  city: Chuo-ku,
  state: Tokyo,
  zipcode: 170-3293,
  country: Japan
)
```

