# Komoju::LineItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **description** | **String** |  | [optional] |
| **quantity** | **Integer** | The default value is 1 if none is given. | [optional] |
| **image** | **String** |  | [optional] |
| **external_product_num** | **String** |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::LineItem.new(
  amount: null,
  description: null,
  quantity: null,
  image: null,
  external_product_num: null
)
```

