# Komoju::SharedDetailsMisc

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **clearings_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **komoju_card_discount_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **chargeback_fixed_fee_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **other_fee_adjustments_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SharedDetailsMisc.new(
  clearings_total_cents: null,
  komoju_card_discount_total_cents: null,
  chargeback_fixed_fee_total_cents: null,
  other_fee_adjustments_total_cents: null,
  total_cents: null
)
```

