# Komoju::ShowBarcodeResponse

## Concrete types

Use one of the following classes when constructing a `ShowBarcodeResponse`:

- [**BarcodePendingResponse**](BarcodePendingResponse.md)
- [**BarcodeReadyResponse**](BarcodeReadyResponse.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-sdk'

Komoju::ShowBarcodeResponse.openapi_one_of
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
require 'komoju-sdk'

Komoju::ShowBarcodeResponse.openapi_discriminator_name
# => :'status'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-sdk'

Komoju::ShowBarcodeResponse.openapi_discriminator_mapping
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
require 'komoju-sdk'

Komoju::ShowBarcodeResponse.build(data)
# => #<BarcodePendingResponse:0x00007fdd4aab02a0>

Komoju::ShowBarcodeResponse.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [BarcodePendingResponse](BarcodePendingResponse.md)
- [BarcodeReadyResponse](BarcodeReadyResponse.md)
- `nil` (if no type matches)

