# Komoju::CustomerSource

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type of the saved payment source. |  |
| **brand** | **String** | Card brand (e.g. \&quot;visa\&quot;, \&quot;mastercard\&quot;). |  |
| **last_four_digits** | **String** | Last four digits of the saved card. |  |
| **month** | **Integer** | Card expiry month (two digits). |  |
| **year** | **Integer** | Card expiry year (two or four digits). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CustomerSource.new(
  type: null,
  brand: null,
  last_four_digits: null,
  month: null,
  year: null
)
```

