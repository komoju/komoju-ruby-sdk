# Komoju::PaymentDetailsBankTransfer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **phone** | **String** | Customer&#39;s phone number |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention, payment instruction, and payment receipt. |  |
| **name** | **String** | Full name of the customer.  This attribute takes precedence over &#x60;given_name&#x60; and &#x60;family_name&#x60;. | [optional] |
| **given_name** | **String** | Given name of the customer.  **Note:** You should only set this attribute if you have separate fields for given name and family name. Otherwise, you should only set the full name via &#x60;name&#x60;. | [optional] |
| **family_name** | **String** | Family name of the customer.  **Note:** You should only set this attribute if you have separate fields for given name and family name. Otherwise, you should only set the full name via &#x60;name&#x60;. | [optional] |
| **given_name_kana** | **String** | Given name of the customer, written in katakana characters. |  |
| **family_name_kana** | **String** | Family name of the customer, written in katakana characters. |  |
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
require 'komoju-sdk'

instance = Komoju::PaymentDetailsBankTransfer.new(
  type: null,
  phone: 08012345678,
  email: example@komoju.com,
  name: John Doe,
  given_name: John,
  family_name: Doe,
  given_name_kana: ジョン,
  family_name_kana: ドー,
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

