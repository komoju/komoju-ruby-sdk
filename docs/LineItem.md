# Komoju::LineItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). | [optional] |
| **description** | **String** | Display name or description of the product or service. | [optional] |
| **quantity** | **Integer** | The default value is 1 if none is given. | [optional] |
| **image** | **String** | URL to an image representing this line item, shown on the session page. | [optional] |
| **external_product_num** | **String** | Merchant&#39;s internal product or SKU identifier. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::LineItem.new(
  amount: null,
  description: null,
  quantity: null,
  image: null,
  external_product_num: null
)
```

