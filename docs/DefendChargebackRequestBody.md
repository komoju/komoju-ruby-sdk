# Komoju::DefendChargebackRequestBody

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **description** | **String** | Explanation of your defense. |  |
| **document** | [**DefendChargebackDocument**](DefendChargebackDocument.md) |  |  |
| **product_name** | **String** | Name of the product or service. | [optional] |
| **shipping_info** | [**DefendChargebackShippingInfo**](DefendChargebackShippingInfo.md) |  | [optional] |
| **recipient_info** | [**DefendChargebackRecipientInfo**](DefendChargebackRecipientInfo.md) |  | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::DefendChargebackRequestBody.new(
  description: null,
  document: null,
  product_name: null,
  shipping_info: null,
  recipient_info: null
)
```

