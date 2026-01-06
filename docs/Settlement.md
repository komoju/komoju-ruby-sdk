# Komoju::Settlement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **resource** | **String** |  |  |
| **reference** | **String** |  |  |
| **merchant_name** | **String** |  |  |
| **company_name** | **String** |  |  |
| **cycle** | **String** |  |  |
| **status** | **String** |  |  |
| **amount** | **String** |  |  |
| **currency** | **String** |  |  |
| **cutoff_time** | **Time** |  |  |
| **created_at** | **Time** |  |  |
| **download** | [**SettlementDownload**](SettlementDownload.md) |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::Settlement.new(
  id: null,
  resource: null,
  reference: null,
  merchant_name: null,
  company_name: null,
  cycle: null,
  status: null,
  amount: null,
  currency: null,
  cutoff_time: null,
  created_at: null,
  download: null
)
```

