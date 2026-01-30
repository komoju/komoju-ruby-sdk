# Komoju::Token

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** |  |  |
| **created_at** | **Time** |  |  |
| **payment_details** | [**TokenPaymentDetails**](TokenPaymentDetails.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Token.new(
  id: null,
  resource: null,
  created_at: null,
  payment_details: null
)
```

