# Komoju::TerminalErrorError

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **code** | **String** | Machine-readable error code. |  |
| **message** | **String** | Human-readable error message. |  |
| **param** | **String** | The parameter that caused the error, if applicable. |  |
| **details** | **Object** | Additional error details. |  |
| **decline_details** | **String** | Detailed decline reason from the EMV terminal. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::TerminalErrorError.new(
  code: null,
  message: null,
  param: null,
  details: null,
  decline_details: null
)
```

