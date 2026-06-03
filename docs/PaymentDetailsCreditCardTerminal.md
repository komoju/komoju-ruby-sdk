# Komoju::PaymentDetailsCreditCardTerminal

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **number** | **String** | Credit card number. |  |
| **month** | **Integer** | Credit card expiration month. | [optional] |
| **year** | **Integer** | Credit card expiration year.  If this value is less than 100, it will be treated as two digits year in the current century. E.g. If current year is &#x60;2024&#x60;, &#x60;99&#x60; means &#x60;2099&#x60;. | [optional] |
| **sequence_number** | **String** | Specify the sequence number from the credit card terminal | [optional] |
| **field55** | **String** | Specify the EMV data produced by the terminal. | [optional] |
| **pos_data_code** | **String** | Specify the POS data code produced by the terminal. | [optional] |
| **track2** | **String** | Specify the data read from track 2 of the payment card. | [optional] |
| **flow_type** | **String** | Specify whether this transaction is a EMV or magnetic stripe transaction.  - Use value \&quot;1\&quot; for EMV transaction. - Use value \&quot;2\&quot; for magnetic stripe transaction. | [optional] |
| **shipping_address_name** | **String** | Shipping address name. This is the recipient&#39;s name. | [optional] |
| **shipping_address_line1** | **String** | Shipping address line 1. | [optional] |
| **shipping_address_line2** | **String** | Shipping address line 2. | [optional] |
| **shipping_address_city** | **String** | Shipping address city. | [optional] |
| **shipping_address_state** | **String** | Shipping address state. | [optional] |
| **shipping_address_zip** | **String** | Shipping address ZIP code. | [optional] |
| **shipping_address_country** | **String** | Shipping address country. | [optional] |
| **billing_address_name** | **String** | Billing address name. This is the paying customer&#39;s name. | [optional] |
| **billing_address_line1** | **String** | Billing address line 1. | [optional] |
| **billing_address_line2** | **String** | Billing address line 2. | [optional] |
| **billing_address_city** | **String** | Billing address city. | [optional] |
| **billing_address_state** | **String** | Billing address state. | [optional] |
| **billing_address_zip** | **String** | Billing address ZIP code. | [optional] |
| **billing_address_country** | **String** | Billing address country. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PaymentDetailsCreditCardTerminal.new(
  type: null,
  number: 4111111111111111,
  month: 10,
  year: 2031,
  sequence_number: 00001,
  field55: 9F0206000000000001,
  pos_data_code: 511101511344,
  track2: 4111111111111111&#x3D;1031111123400001230,
  flow_type: 1,
  shipping_address_name: Taro Tanaka,
  shipping_address_line1: 5-2-1 Ginza,
  shipping_address_line2: 3rd floor,
  shipping_address_city: Chuo-ku,
  shipping_address_state: Tokyo,
  shipping_address_zip: 170-3293,
  shipping_address_country: Japan,
  billing_address_name: Taro Tanaka,
  billing_address_line1: 5-2-1 Ginza,
  billing_address_line2: 3rd floor,
  billing_address_city: Chuo-ku,
  billing_address_state: Tokyo,
  billing_address_zip: 170-3293,
  billing_address_country: Japan
)
```

