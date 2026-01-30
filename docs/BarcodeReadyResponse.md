# Komoju::BarcodeReadyResponse

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **status** | **String** | Barcode is available |  |
| **expires_at** | **Time** | Barcode cannot be used for payment after this time |  |
| **image** | **String** | Base64 encoded PNG image (width: 750px, height: 150px). This value can be used as the &#x60;src&#x60; attribute of an HTML &#x60;&lt;img&gt;&#x60; tag. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::BarcodeReadyResponse.new(
  status: null,
  expires_at: null,
  image: null
)
```

