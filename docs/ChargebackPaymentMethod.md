# Komoju::ChargebackPaymentMethod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type slug (e.g. \&quot;credit_card\&quot;). |  |
| **brand** | **String** | Card brand, or null if not applicable. |  |
| **last_four_digits** | **String** | Last four digits of the card, or null if not applicable. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackPaymentMethod.new(
  type: null,
  brand: null,
  last_four_digits: null
)
```

