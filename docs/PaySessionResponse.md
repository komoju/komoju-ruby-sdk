# Komoju::PaySessionResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **redirect_url** | **String** |  |  |
| **status** | [**SessionStatus**](SessionStatus.md) |  |  |
| **payment** | [**Payment**](Payment.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::PaySessionResponse.new(
  redirect_url: null,
  status: null,
  payment: null
)
```

