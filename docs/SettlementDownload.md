# Komoju::SettlementDownload

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **csv** | **String** | URL to download this settlement in CSV format, or null if unavailable. |  |
| **xls** | **String** | URL to download this settlement in XLS format, or null if unavailable. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SettlementDownload.new(
  csv: null,
  xls: null
)
```

