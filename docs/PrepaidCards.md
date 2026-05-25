# Komoju::PrepaidCards

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **last_four_digits** | **String** | Last four digits of the prepaid card number. | [optional] |
| **points** | **Integer** | Points or remaining balance on this prepaid card. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::PrepaidCards.new(
  last_four_digits: null,
  points: null
)
```

