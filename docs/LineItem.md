# Komoju::LineItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **amount** | **Integer** | Must be equal or greater than 0. Always in lowest denomination of the currency (e.g. cents for USD). |  |
| **description** | **String** |  |  |
| **quantity** | **Integer** |  |  |
| **image** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::LineItem.new(
  amount: null,
  description: null,
  quantity: null,
  image: null
)
```

