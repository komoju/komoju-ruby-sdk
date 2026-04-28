# Komoju::SettlementList

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **resource** | **String** | Resource type name, always \&quot;settlement_list\&quot;. |  |
| **data** | [**Array&lt;Settlement&gt;**](Settlement.md) | Array of settlement objects for this page. |  |
| **start_time** | **Time** | Start of the time range for records in this response. |  |
| **end_time** | **Time** | End of the time range for records in this response. |  |
| **total** | **Integer** | Total number of records matching the query. |  |
| **page** | **Integer** | Current page number. |  |
| **per_page** | **Integer** | Number of results per page. |  |
| **last_page** | **Integer** | Last available page number. |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SettlementList.new(
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

