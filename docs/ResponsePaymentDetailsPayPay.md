# Komoju::ResponsePaymentDetailsPayPay

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. |  |
| **redirect_url** | **String** | URL to redirect the customer to for completing the PayPay payment. | [optional] |
| **external_payment_id** | **String** | Payment identifier returned by PayPay. | [optional] |
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

instance = Komoju::ResponsePaymentDetailsPayPay.new(
  type: null,
  email: example@komoju.com,
  redirect_url: null,
  external_payment_id: null,
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

