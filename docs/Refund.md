# Komoju::Refund

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric refund identifier. |  |
| **resource** | **String** | Resource name. Will always be &#x60;refund&#x60;. |  |
| **amount** | **Integer** | The refund amount with tax included, greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **payment** | **String** | A unique 25-character alphanumeric payment identifier. |  |
| **description** | **String** | Description of the refund. |  |
| **created_at** | **Time** |  |  |
| **chargeback** | **Boolean** | Denotes if this refund was created due to a chargeback. |  |
| **platform_details** | [**RefundPlatformDetails**](RefundPlatformDetails.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Refund.new(
  id: ref442o1crn4qn3a3c7gspfik,
  resource: null,
  amount: 1000,
  currency: null,
  payment: pay3fj6nnhvws08idzacf6et8,
  description: Full refund,
  created_at: null,
  chargeback: false,
  platform_details: null
)
```

