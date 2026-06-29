# Komoju::ChargebackDefenseShippingInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_name** | **String** | Shipping carrier company name, or null. |  |
| **shipping_date** | **String** | Date the item was shipped (e.g. 2026-05-20), or null. |  |
| **tracking_number** | **String** | Carrier tracking number, or null. |  |
| **shipping_address** | **String** | Destination shipping address, or null. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackDefenseShippingInfo.new(
  company_name: null,
  shipping_date: null,
  tracking_number: null,
  shipping_address: null
)
```

