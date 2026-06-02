# Komoju::PlatformDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submerchants** | [**Array&lt;Submerchant&gt;**](Submerchant.md) | Array of submerchant split configurations for this platform payment. |  |
| **processing_merchant_id** | **String** | A unique 25-character alphanumeric resource identifier. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PlatformDetails.new(
  submerchants: null,
  processing_merchant_id: null
)
```

