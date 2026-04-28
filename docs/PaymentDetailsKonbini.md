# Komoju::PaymentDetailsKonbini

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **store** | **String** | Specify the name of convenience store user will make payment from. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention, payment instruction, and payment receipt. |  |
| **phone** | **String** | Customer&#39;s phone number | [optional] |
| **family_name** | **String** | Family name of the customer. It will appear on the Konbini payment receipt. | [optional] |
| **given_name** | **String** | Given name of the customer. It will appear on the Konbini payment receipt. | [optional] |
| **expiry_days** | **Integer** | Specify how many days before the payment expires.  If this value is omitted, the default expiry day shown in the merchant dashboard will be used. | [optional] |
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

instance = Komoju::PaymentDetailsKonbini.new(
  type: null,
  store: null,
  email: example@komoju.com,
  phone: 08012345678,
  family_name: Doe,
  given_name: John,
  expiry_days: 7,
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

