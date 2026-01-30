# Komoju::CreatePaymentRequest

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::CreatePaymentRequest.openapi_one_of
# =>
# [
#   :'CreatePaymentRequestWithCustomer',
#   :'CreatePaymentRequestWithPaymentDetails'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::CreatePaymentRequest.build(data)
# => #<CreatePaymentRequestWithCustomer:0x00007fdd4aab02a0>

Komoju::CreatePaymentRequest.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `CreatePaymentRequestWithCustomer`
- `CreatePaymentRequestWithPaymentDetails`
- `nil` (if no type matches)

