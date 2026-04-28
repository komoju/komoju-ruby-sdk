# Komoju::PaymentDetailsOnlyCreditCards

## Concrete types

Use one of the following classes when constructing a `PaymentDetailsOnlyCreditCards`:

- [**PaymentDetailsCreditCard**](PaymentDetailsCreditCard.md)
- [**PaymentDetailsCreditCardBrazil**](PaymentDetailsCreditCardBrazil.md)
- [**PaymentDetailsCreditCardKorea**](PaymentDetailsCreditCardKorea.md)
- [**PaymentDetailsCreditCardTerminal**](PaymentDetailsCreditCardTerminal.md)

## Class instance methods

### `openapi_one_of`

Returns the list of classes defined in oneOf.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::PaymentDetailsOnlyCreditCards.openapi_one_of
# =>
# [
#   :'PaymentDetailsCreditCard',
#   :'PaymentDetailsCreditCardBrazil',
#   :'PaymentDetailsCreditCardKorea',
#   :'PaymentDetailsCreditCardTerminal'
# ]
```

### `openapi_discriminator_name`

Returns the discriminator's property name.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::PaymentDetailsOnlyCreditCards.openapi_discriminator_name
# => :'type'
```

### `openapi_discriminator_name`

Returns the discriminator's mapping.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::PaymentDetailsOnlyCreditCards.openapi_discriminator_mapping
# =>
# {
#   :'credit_card' => :'PaymentDetailsCreditCard',
#   :'credit_card_brazil' => :'PaymentDetailsCreditCardBrazil',
#   :'credit_card_korea' => :'PaymentDetailsCreditCardKorea',
#   :'credit_card_terminal' => :'PaymentDetailsCreditCardTerminal'
# }
```

### build

Find the appropriate object from the `openapi_one_of` list and casts the data into it.

#### Example

```ruby
require 'komoju-ruby-sdk'

Komoju::PaymentDetailsOnlyCreditCards.build(data)
# => #<PaymentDetailsCreditCard:0x00007fdd4aab02a0>

Komoju::PaymentDetailsOnlyCreditCards.build(data_that_doesnt_match)
# => nil
```

#### Parameters

| Name | Type | Description |
| ---- | ---- | ----------- |
| **data** | **Mixed** | data to be matched against the list of oneOf items |

#### Return type

- [PaymentDetailsCreditCard](PaymentDetailsCreditCard.md)
- [PaymentDetailsCreditCardBrazil](PaymentDetailsCreditCardBrazil.md)
- [PaymentDetailsCreditCardKorea](PaymentDetailsCreditCardKorea.md)
- [PaymentDetailsCreditCardTerminal](PaymentDetailsCreditCardTerminal.md)
- `nil` (if no type matches)

