# Komoju::ResponsePaymentDetailsCreditCard

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **brand** | **String** | Card brand (e.g. \&quot;visa\&quot;, \&quot;mastercard\&quot;, \&quot;jcb\&quot;). |  |
| **last_four_digits** | **String** | Last four digits of the card number. |  |
| **month** | **Integer** | Credit card expiration month. |  |
| **year** | **Integer** | Credit card expiration year.  If this value is less than 100, it will be treated as two digits year in the current century. E.g. If current year is &#x60;2024&#x60;, &#x60;99&#x60; means &#x60;2099&#x60;. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. |  |
| **verification_value** | **String** |  | [optional] |
| **name** | **String** | Full name of the customer.  This attribute takes precedence over &#x60;given_name&#x60; and &#x60;family_name&#x60;. | [optional] |
| **given_name** | **String** | Given name of the customer. | [optional] |
| **family_name** | **String** | Family name of the customer. | [optional] |
| **expiry_days** | **Integer** |  | [optional] |
| **intent** | **String** |  | [optional] |
| **initiator** | **String** |  | [optional] |
| **usage** | **String** |  | [optional] |
| **scheme_reference** | **String** |  | [optional] |
| **installments** | [**Installments**](Installments.md) |  | [optional] |
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

instance = Komoju::ResponsePaymentDetailsCreditCard.new(
  type: null,
  brand: null,
  last_four_digits: null,
  month: 10,
  year: 2031,
  email: example@komoju.com,
  verification_value: null,
  name: John Doe,
  given_name: John,
  family_name: Doe,
  expiry_days: null,
  intent: null,
  initiator: null,
  usage: null,
  scheme_reference: null,
  installments: null,
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

