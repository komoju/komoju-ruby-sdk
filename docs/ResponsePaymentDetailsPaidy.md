# Komoju::ResponsePaymentDetailsPaidy

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type. |  |
| **email** | **String** | Customer&#39;s email address. Will be used for fraud prevention and payment receipt. |  |
| **redirect_url** | **String** | URL to redirect the customer to for completing the Paidy payment. | [optional] |
| **shipping_address_name** | **String** | Shipping address name.  This is the recipient&#39;s name. | [optional] |
| **shipping_address_line1** | **String** | Shipping address line 1.  For Japanese addresses: building name, apartment number. Required for physical products. | [optional] |
| **shipping_address_line2** | **String** | Shipping address line 2.  For Japanese addresses: district, land number, land number extension. | [optional] |
| **shipping_address_city** | **String** | Shipping address city.  Name of city, municipality, or village. Required for physical products. | [optional] |
| **shipping_address_state** | **String** | Shipping address state / prefecture.  Required for physical products. | [optional] |
| **shipping_address_zip** | **String** | Shipping address ZIP code, in a 7-digit format (NNN-NNNN). Required for physical products. | [optional] |
| **shipping_address_country** | **String** | Shipping address country. Required for physical products. | [optional] |
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

instance = Komoju::ResponsePaymentDetailsPaidy.new(
  type: null,
  email: example@komoju.com,
  redirect_url: null,
  shipping_address_name: Taro Tanaka,
  shipping_address_line1: Ichigo Kichijoji Bldg. 4F,
  shipping_address_line2: 5-10, Kichijoji Honcho 2-chome,
  shipping_address_city: Musashino-shi,
  shipping_address_state: Tokyo-to,
  shipping_address_zip: 180-0004,
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

