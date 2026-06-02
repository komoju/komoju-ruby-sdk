# Komoju::SharedDetailsPayments

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **captured_amount_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **processing_fees_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SharedDetailsPayments.new(
  captured_amount_total_cents: null,
  processing_fees_cents: null,
  total_cents: null
)
```

