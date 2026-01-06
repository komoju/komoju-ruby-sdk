# Komoju::DisbursementList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **resource** | **String** |  |  |
| **data** | [**Array&lt;Disbursement&gt;**](Disbursement.md) |  |  |
| **start_time** | **Time** |  |  |
| **end_time** | **Time** |  |  |
| **total** | **Integer** |  |  |
| **page** | **Integer** |  |  |
| **per_page** | **Integer** |  |  |
| **last_page** | **Integer** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::DisbursementList.new(
  resource: null,
  data: null,
  start_time: null,
  end_time: null,
  total: null,
  page: null,
  per_page: null,
  last_page: null
)
```

