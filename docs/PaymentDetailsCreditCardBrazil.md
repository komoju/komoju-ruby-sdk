# Komoju::PaymentDetailsCreditCardBrazil

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. |  |
| **number** | **String** | Credit card number. |  |
| **month** | **Integer** | Credit card expiration month. |  |
| **year** | **Integer** | Credit card expiration year.  If this value is less than 100, it will be treated as two digits year in the current century. E.g. If current year is &#x60;2024&#x60;, &#x60;99&#x60; means &#x60;2099&#x60;. |  |
| **verification_value** | **String** | Credit card verification value (Also known as CVV2 or CVC2). |  |
| **name** | **String** | Full name of the customer.  This attribute takes precedence over &#x60;given_name&#x60; and &#x60;family_name&#x60;. |  |
| **cpf_or_cnpj** | **String** | Specify customer&#39;s CPF or CNPJ. |  |
| **customer_ip** | **String** | Specify customer&#39;s IPv4 or IPv6-formatted IP address of the customer at the time of payment. |  |
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

instance = Komoju::PaymentDetailsCreditCardBrazil.new(
  type: null,
  email: example@komoju.com,
  number: 4111111111111111,
  month: 10,
  year: 2031,
  verification_value: 000,
  name: John Doe,
  cpf_or_cnpj: 999999999-99,
  customer_ip: ::1,
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

