# Komoju::CreateSessionRequest

## Concrete types

Use one of the following classes when constructing a `CreateSessionRequest`:

- [**CreateSessionRequestWithCustomerMode**](CreateSessionRequestWithCustomerMode.md)
- [**CreateSessionRequestWithCustomerPaymentMode**](CreateSessionRequestWithCustomerPaymentMode.md)
- [**CreateSessionRequestWithPaymentMode**](CreateSessionRequestWithPaymentMode.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-sdk'

Komoju::CreateSessionRequest.openapi_one_of
# =>
# [
#   :'CreateSessionRequestWithCustomerMode',
#   :'CreateSessionRequestWithCustomerPaymentMode',
#   :'CreateSessionRequestWithPaymentMode'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'komoju-sdk'

Komoju::CreateSessionRequest.openapi_discriminator_name
# => :'mode'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-sdk'

Komoju::CreateSessionRequest.openapi_discriminator_mapping
# =>
# {
#   :'customer' => :'CreateSessionRequestWithCustomerMode',
#   :'customer_payment' => :'CreateSessionRequestWithCustomerPaymentMode',
#   :'payment' => :'CreateSessionRequestWithPaymentMode'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-sdk'

Komoju::CreateSessionRequest.build(data)
# => #<CreateSessionRequestWithCustomerMode:0x00007fdd4aab02a0>

Komoju::CreateSessionRequest.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [CreateSessionRequestWithCustomerMode](CreateSessionRequestWithCustomerMode.md)
- [CreateSessionRequestWithCustomerPaymentMode](CreateSessionRequestWithCustomerPaymentMode.md)
- [CreateSessionRequestWithPaymentMode](CreateSessionRequestWithPaymentMode.md)
- `nil` (if no type matches)

