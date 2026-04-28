# Komoju::SubmittedFieldAllOfValue

## Concrete types

Use one of the following classes when constructing a `SubmittedFieldAllOfValue`:

- [**Boolean**](Boolean.md)
- [**Integer**](Integer.md)
- [**String**](String.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::SubmittedFieldAllOfValue.openapi_one_of
# =>
# [
#   :'Boolean',
#   :'Integer',
#   :'String'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::SubmittedFieldAllOfValue.build(data)
# => #<Boolean:0x00007fdd4aab02a0>

Komoju::SubmittedFieldAllOfValue.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [Boolean](Boolean.md)
- [Integer](Integer.md)
- [String](String.md)
- `nil` (if no type matches)

