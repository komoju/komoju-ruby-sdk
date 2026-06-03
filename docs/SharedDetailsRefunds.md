# Komoju::SharedDetailsRefunds

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **refunded_amount_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **refund_processing_fees_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **refunded_customer_fees_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SharedDetailsRefunds.new(
  refunded_amount_total_cents: null,
  refund_processing_fees_cents: null,
  refunded_customer_fees_cents: null,
  total_cents: null
)
```

