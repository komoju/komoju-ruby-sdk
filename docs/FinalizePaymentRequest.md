# Komoju::FinalizePaymentRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **capture** | **Boolean** |  | [optional] |
| **ac_type** | **String** | EMV chip card action code: TC (approved), AAC (declined), or fault. |  |
| **field55** | **String** | EMV tag 55 data from the chip card transaction. |  |
| **track2** | **String** | Track 2 magnetic stripe equivalent data from the chip card. |  |
| **metadata** | **Object** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::FinalizePaymentRequest.new(
  capture: null,
  ac_type: null,
  field55: null,
  track2: null,
  metadata: null
)
```

