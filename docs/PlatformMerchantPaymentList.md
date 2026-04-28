# Komoju::PlatformMerchantPaymentList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **resource** | **String** | Resource type name for this list. |  |
| **total** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **page** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **per_page** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **last_page** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **data** | [**Array&lt;PlatformPayment&gt;**](PlatformPayment.md) | Array of payment objects for this page. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PlatformMerchantPaymentList.new(
  resource: null,
  total: null,
  page: null,
  per_page: null,
  last_page: null,
  data: null
)
```

