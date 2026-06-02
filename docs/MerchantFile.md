# Komoju::MerchantFile

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique identifier for this file. |  |
| **resource** | **String** | Resource type name, always \&quot;file\&quot;. |  |
| **filename** | **String** | Original filename of the uploaded file. |  |
| **size** | **Integer** | File size in bytes. |  |
| **mime_type** | **String** | MIME type of the uploaded file (e.g. \&quot;application/pdf\&quot;). |  |
| **created_at** | **Time** | Timestamp when the file was uploaded. |  |
| **updated_at** | **Time** | Timestamp when the file record was last updated. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::MerchantFile.new(
  id: null,
  resource: null,
  filename: null,
  size: null,
  mime_type: null,
  created_at: null,
  updated_at: null
)
```

