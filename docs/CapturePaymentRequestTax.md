# Komoju::CapturePaymentRequestTax

## Concrete types

Use one of the following classes when constructing a `CapturePaymentRequestTax`:

- [**Auto**](Auto.md)
- [**Integer**](Integer.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::CapturePaymentRequestTax.openapi_one_of
# =>
# [
#   :'Auto',
#   :'Integer'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::CapturePaymentRequestTax.build(data)
# => #<Auto:0x00007fdd4aab02a0>

Komoju::CapturePaymentRequestTax.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [Auto](Auto.md)
- [Integer](Integer.md)
- `nil` (if no type matches)

