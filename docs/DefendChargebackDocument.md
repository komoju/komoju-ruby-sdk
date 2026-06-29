# Komoju::DefendChargebackDocument

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **document_base64** | **String** | Base64-encoded file contents. Must be 15 MB or less. Supported types: PDF, JPG/JPEG, PNG, GIF. |  |
| **filename** | **String** | Original file name. | [optional] |
| **content_type** | **String** | MIME type of the file. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::DefendChargebackDocument.new(
  document_base64: null,
  filename: null,
  content_type: null
)
```

