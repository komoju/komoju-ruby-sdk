# Komoju::PaymentDetailsCreditCard

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. | [optional] |
| **number** | **String** | Credit card number. |  |
| **month** | **Integer** | Credit card expiration month. |  |
| **year** | **Integer** | Credit card expiration year.  If this value is less than 100, it will be treated as two digits year in the current century. E.g. If current year is &#x60;2024&#x60;, &#x60;99&#x60; means &#x60;2099&#x60;. |  |
| **verification_value** | **String** | Credit card verification value (Also known as CVV2 or CVC2). | [optional] |
| **name** | **String** | Full name of the customer.  This attribute takes precedence over &#x60;given_name&#x60; and &#x60;family_name&#x60;. | [optional] |
| **given_name** | **String** | Given name of the customer.  **Note:** You should only set this attribute if you have separate fields for given name and family name. Otherwise, you should only set the full name via &#x60;name&#x60;. | [optional] |
| **family_name** | **String** | Family name of the customer.  **Note:** You should only set this attribute if you have separate fields for given name and family name. Otherwise, you should only set the full name via &#x60;name&#x60;. | [optional] |
| **expiry_days** | **Integer** | If the payment is not immediately captured, specify how many days before the payment expires.  If this value is omitted, the default expiry day shown in the merchant dashboard will be used. | [optional] |
| **intent** | [**Intent**](Intent.md) |  | [optional] |
| **initiator** | **String** | Specify the initiator of this payment.  Specifying this attribute can increase authorization credit card payments authorization rates, especially when using a stored card.  You can set this value to &#x60;customer&#x60; when the payment is being made for one-time goods or service purchase, or &#x60;merchant&#x60; for recurring subscription or installment payments. | [optional] |
| **usage** | **String** | Specify whether this payment is the first (&#x60;first&#x60;) or a subsequent payment in a series (&#x60;used&#x60;).  Specifying this attribute can increase authorization credit card payments authorization rates, especially when using a stored card. | [optional] |
| **scheme_reference** | **String** | Specify a scheme reference value, which is used to track the chain of multiple related payments.  This value can be subscription number for a recurring subscription payments, or installment agreement number for installment payments.  Specifying this attribute can increase authorization credit card payments authorization rates, especially when using a stored card. | [optional] |
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
require 'komoju-ruby-sdk'

instance = Komoju::PaymentDetailsCreditCard.new(
  type: null,
  email: komoju@degica.com,
  number: 4111111111111111,
  month: 10,
  year: 2031,
  verification_value: 000,
  name: John Doe,
  given_name: John,
  family_name: Doe,
  expiry_days: 2,
  intent: null,
  initiator: null,
  usage: null,
  scheme_reference: SUBSCRIPTION-1234,
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

