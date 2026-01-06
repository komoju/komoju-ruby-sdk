# Komoju::Balance

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  |  |
| **payment_total** | **String** |  |  |
| **fund_transfer_total** | **String** |  |  |
| **payment_fee_total** | **String** |  |  |
| **refund_total** | **String** |  |  |
| **refund_fee_total** | **String** |  |  |
| **refunded_customer_fee_total** | **String** |  |  |
| **correction_total** | **String** |  |  |
| **tax_total** | **String** |  |  |
| **balance_total** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Balance.new(
  currency: null,
  payment_total: null,
  fund_transfer_total: null,
  payment_fee_total: null,
  refund_total: null,
  refund_fee_total: null,
  refunded_customer_fee_total: null,
  correction_total: null,
  tax_total: null,
  balance_total: null
)
```

