# Komoju::PaymentMethodBrands

## Concrete types

Use one of the following classes when constructing a `PaymentMethodBrands`:

- [**Array<Object>**](Array<Object>.md)
- [**Array<String>**](Array<String>.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::PaymentMethodBrands.openapi_one_of
# =>
# [
#   :'Array<Object>',
#   :'Array<String>'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::PaymentMethodBrands.build(data)
# => #<Array<Object>:0x00007fdd4aab02a0>

Komoju::PaymentMethodBrands.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [Array<Object>](Array<Object>.md)
- [Array<String>](Array<String>.md)
- `nil` (if no type matches)

