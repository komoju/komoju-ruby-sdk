# Komoju::DefendChargebackShippingInfo

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **company_name** | **String** | Shipping carrier company name. | [optional] |
| **shipping_date** | **String** | Date the item was shipped (e.g. 2026-05-20). | [optional] |
| **tracking_number** | **String** | Carrier tracking number. | [optional] |
| **shipping_address** | **String** | Destination shipping address. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::DefendChargebackShippingInfo.new(
  company_name: null,
  shipping_date: null,
  tracking_number: null,
  shipping_address: null
)
```

