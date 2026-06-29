# Komoju::ChargebackDefense

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **product_name** | **String** | Name of the product or service, or null if not provided. |  |
| **reason** | **String** | The merchant&#39;s defense reason. |  |
| **shipping_info** | [**ChargebackDefenseShippingInfo**](ChargebackDefenseShippingInfo.md) |  |  |
| **recipient_info** | [**ChargebackDefenseRecipientInfo**](ChargebackDefenseRecipientInfo.md) |  |  |
| **documents** | [**Array&lt;ChargebackDefenseDocument&gt;**](ChargebackDefenseDocument.md) | Supporting documents submitted with the defense. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackDefense.new(
  product_name: null,
  reason: null,
  shipping_info: null,
  recipient_info: null,
  documents: null
)
```

