# Komoju::LiveApplication

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **status** | [**LiveApplicationStatus**](LiveApplicationStatus.md) |  |  |
| **payments_enabled** | **Boolean** |  |  |
| **payouts_enabled** | **Boolean** |  |  |
| **requested_fields** | [**Array&lt;Field&gt;**](Field.md) |  |  |
| **newly_requested_fields** | [**Array&lt;Field&gt;**](Field.md) |  |  |
| **errored_fields** | [**Array&lt;ErroredField&gt;**](ErroredField.md) |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::LiveApplication.new(
  merchant_id: null,
  status: null,
  payments_enabled: null,
  payouts_enabled: null,
  requested_fields: null,
  newly_requested_fields: null,
  errored_fields: null
)
```

