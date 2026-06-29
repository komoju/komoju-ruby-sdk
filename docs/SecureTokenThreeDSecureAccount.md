# Komoju::SecureTokenThreeDSecureAccount

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **acquirer_mid** | **String** | Acquirer Merchant ID, or null if not configured. |  |
| **acquirer_bin** | **String** | Acquirer BIN, or null if not configured. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SecureTokenThreeDSecureAccount.new(
  acquirer_mid: null,
  acquirer_bin: null
)
```

