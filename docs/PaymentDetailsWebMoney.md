# Komoju::PaymentDetailsWebMoney

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type.  **Note:** This payment method support updating the payment with additional prepaid cards to cover the total balance. In case of insufficient funds, the payment status will be &#x60;pending&#x60;.  The &#x60;payment_details&#x60; in the response will also include these two attributes:  - &#x60;short_amount&#x60;: The amount that the payment is short by. - &#x60;prepaid_cards&#x60;: A list of prepaid cards used in the transaction.  Please see the integration document for more details. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. | [optional] |
| **prepaid_number** | **String** | Prepaid card number. |  |
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

instance = Komoju::PaymentDetailsWebMoney.new(
  type: null,
  email: example@komoju.com,
  prepaid_number: 1234567890abcdef,
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

