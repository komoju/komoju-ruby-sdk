# Komoju::PlatformDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **submerchants** | [**Array&lt;Submerchant&gt;**](Submerchant.md) |  |  |
| **processing_merchant_id** | **String** | A unique 25-character alphanumeric resource identifier. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PlatformDetails.new(
  submerchants: null,
  processing_merchant_id: null
)
```

