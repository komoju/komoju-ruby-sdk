# Komoju::CreateSecureTokenRequestWithCustomer

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **customer** | **String** | To use instead of &#x60;payment_details&#x60;, specify customer&#39;s identifier for this SecureToken.  This identifier can be obtained from [Customer: Create](https://doc.komoju.com/reference/createcustomer) endpoint. |  |
| **return_url** | **String** |  |  |
| **platform_details** | [**ProcessingMerchant**](ProcessingMerchant.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CreateSecureTokenRequestWithCustomer.new(
  amount: null,
  currency: null,
  customer: cust14ur4hvws08idzacf6et8,
  return_url: null,
  platform_details: null
)
```

