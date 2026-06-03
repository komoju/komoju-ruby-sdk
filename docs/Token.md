# Komoju::Token

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;token\&quot;. |  |
| **created_at** | **Time** | Timestamp when the token was created. |  |
| **payment_details** | [**TokenPaymentDetails**](TokenPaymentDetails.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Token.new(
  id: null,
  resource: null,
  created_at: null,
  payment_details: null
)
```

