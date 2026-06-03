# Komoju::MerchantSubmissionStatus

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **merchant_id** | **String** | Identifier of the merchant whose submission status is being reported. |  |
| **status** | **String** | Current status of the merchant&#39;s live application submission. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::MerchantSubmissionStatus.new(
  merchant_id: null,
  status: null
)
```

