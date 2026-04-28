# Komoju::SharedDetailsPlatformModel

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **fund_transfer_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **payment_share_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **payment_share_refund_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **platform_fee_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **platform_fee_refund_total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **submerchant_management_fees_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **total_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SharedDetailsPlatformModel.new(
  fund_transfer_total_cents: null,
  payment_share_total_cents: null,
  payment_share_refund_total_cents: null,
  platform_fee_total_cents: null,
  platform_fee_refund_total_cents: null,
  submerchant_management_fees_cents: null,
  total_cents: null
)
```

