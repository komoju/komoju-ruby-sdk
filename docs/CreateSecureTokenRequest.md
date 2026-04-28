# Komoju::CreateSecureTokenRequest

## Concrete types

Use one of the following classes when constructing a `CreateSecureTokenRequest`:

- [**CreateSecureTokenRequestWithCustomer**](CreateSecureTokenRequestWithCustomer.md)
- [**CreateSecureTokenRequestWithPaymentDetails**](CreateSecureTokenRequestWithPaymentDetails.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::CreateSecureTokenRequest.openapi_one_of
# =>
# [
#   :'CreateSecureTokenRequestWithCustomer',
#   :'CreateSecureTokenRequestWithPaymentDetails'
# ]
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::CreateSecureTokenRequest.build(data)
# => #<CreateSecureTokenRequestWithCustomer:0x00007fdd4aab02a0>

Komoju::CreateSecureTokenRequest.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [CreateSecureTokenRequestWithCustomer](CreateSecureTokenRequestWithCustomer.md)
- [CreateSecureTokenRequestWithPaymentDetails](CreateSecureTokenRequestWithPaymentDetails.md)
- `nil` (if no type matches)

