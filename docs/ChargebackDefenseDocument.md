# Komoju::ChargebackDefenseDocument

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **file_name** | **String** | Stored file name. |  |
| **content_type** | **String** | MIME type of the document. |  |
| **file_size** | **Integer** | File size in bytes. |  |
| **uploaded_at** | **Time** | When the document was uploaded. |  |
| **url** | **String** | Temporary signed URL to download the document. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::ChargebackDefenseDocument.new(
  file_name: null,
  content_type: null,
  file_size: null,
  uploaded_at: null,
  url: null
)
```

