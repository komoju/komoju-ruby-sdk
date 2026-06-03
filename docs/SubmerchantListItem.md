# Komoju::SubmerchantListItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | Unique identifier for this sub-merchant. |  |
| **live** | **Boolean** | Whether this merchant is operating in live (production) mode. |  |
| **created_at** | **Time** | Timestamp when this merchant was created. |  |
| **updated_at** | **Time** | Timestamp when this merchant record was last updated. |  |
| **account_id** | **String** | Account identifier associated with this merchant. |  |
| **name** | **String** | Display name of the sub-merchant. |  |
| **platform_role** | [**MerchantRole**](MerchantRole.md) |  |  |
| **status** | **String** | Account application status of the merchant. |  |
| **payments_enabled** | **Boolean** | Whether payments are enabled for this merchant. |  |
| **payouts_enabled** | **Boolean** | Whether payouts are enabled for this merchant. |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SubmerchantListItem.new(
  id: null,
  live: null,
  created_at: null,
  updated_at: null,
  account_id: null,
  name: null,
  platform_role: null,
  status: null,
  payments_enabled: null,
  payouts_enabled: null
)
```

