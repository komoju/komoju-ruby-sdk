# Komoju::LiveApplication

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** |  |  |
| **status** | **String** |  |  |
| **payments_enabled** | **Boolean** |  |  |
| **payouts_enabled** | **Boolean** |  |  |
| **required_fields** | **Array&lt;String&gt;** |  |  |
| **newly_required_fields** | **Array&lt;String&gt;** |  |  |
| **errored_fields** | **Array&lt;String&gt;** |  |  |
| **submitted_fields** | [**Array&lt;LiveApplicationSubmittedFieldsInner&gt;**](LiveApplicationSubmittedFieldsInner.md) |  |  |
| **position** | **Integer** |  |  |
| **value** | **Boolean** |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::LiveApplication.new(
  merchant_id: null,
  status: null,
  payments_enabled: null,
  payouts_enabled: null,
  required_fields: null,
  newly_required_fields: null,
  errored_fields: null,
  submitted_fields: null,
  position: null,
  value: null
)
```

