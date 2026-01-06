# Komoju::PaymentDetailsCreditCardTerminal

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** |  |  |
| **number** | **String** |  |  |
| **month** | **Integer** |  | [optional] |
| **year** | **Integer** |  | [optional] |
| **sequence_number** | **String** |  | [optional] |
| **field55** | **String** | \&quot;Field 55\&quot; is the EMV data produced by the terminal. | [optional] |
| **pos_data_code** | **String** |  | [optional] |
| **track2** | **String** |  | [optional] |
| **flow_type** | **String** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::PaymentDetailsCreditCardTerminal.new(
  type: null,
  number: null,
  month: null,
  year: null,
  sequence_number: null,
  field55: null,
  pos_data_code: null,
  track2: null,
  flow_type: null
)
```

