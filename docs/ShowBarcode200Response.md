# Komoju::ShowBarcode200Response

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ShowBarcode200Response.openapi_one_of
# =>
# [
#   :'BarcodePendingResponse',
#   :'BarcodeReadyResponse'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ShowBarcode200Response.openapi_discriminator_name
# => :'status'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ShowBarcode200Response.openapi_discriminator_mapping
# =>
# {
#   :'pending' => :'BarcodePendingResponse',
#   :'ready' => :'BarcodeReadyResponse'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::ShowBarcode200Response.build(data)
# => #<BarcodePendingResponse:0x00007fdd4aab02a0>

Komoju::ShowBarcode200Response.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- `BarcodePendingResponse`
- `BarcodeReadyResponse`
- `nil` (if no type matches)

