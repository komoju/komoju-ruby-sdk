# Komoju::CreateSecureTokenRequestWithPaymentDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **payment_details** | [**PaymentDetailsOnlyCreditCards**](PaymentDetailsOnlyCreditCards.md) |  |  |
| **return_url** | **String** |  |  |
| **platform_details** | [**ProcessingMerchant**](ProcessingMerchant.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::CreateSecureTokenRequestWithPaymentDetails.new(
  amount: null,
  currency: null,
  payment_details: null,
  return_url: null,
  platform_details: null
)
```

