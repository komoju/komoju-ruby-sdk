# Komoju::CreatePaymentRequestWithPaymentDetailsTax

## Concrete types

Use one of the following classes when constructing a `CreatePaymentRequestWithPaymentDetailsTax`:

- [**Auto**](Auto.md)
- [**Integer**](Integer.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-sdk'

Komoju::CreatePaymentRequestWithPaymentDetailsTax.openapi_one_of
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
require 'komoju-sdk'

Komoju::CreatePaymentRequestWithPaymentDetailsTax.build(data)
# => #<Auto:0x00007fdd4aab02a0>

Komoju::CreatePaymentRequestWithPaymentDetailsTax.build(data_that_doesnt_match)
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

