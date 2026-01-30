# Komoju::SerializedSubmerchantExpirySettingsInner

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name** | **String** |  |  |
| **slug** | **String** |  |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **expiry_days** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **default_expiry_days** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SerializedSubmerchantExpirySettingsInner.new(
  name: null,
  slug: null,
  currency: null,
  expiry_days: null,
  default_expiry_days: null
)
```

