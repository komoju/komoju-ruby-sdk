# Komoju::SharedDetailsDisbursements

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **disbursement_amount_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **disbursement_fee_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SharedDetailsDisbursements.new(
  disbursement_amount_total_cents: null,
  disbursement_fee_total_cents: null,
  total_cents: null
)
```

