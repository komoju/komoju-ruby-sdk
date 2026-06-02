# Komoju::APIErrorBody

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Machine-readable error code. |  |
| **message** | **String** | Human-readable error message. |  |
| **param** | **String** | The parameter that caused the error, if applicable. |  |
| **details** | **Object** | Additional error details. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::APIErrorBody.new(
  code: null,
  message: null,
  param: null,
  details: null
)
```

