# Komoju::SubmerchantListItem

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** |  |  |
| **live** | **Boolean** |  |  |
| **created_at** | **Time** |  |  |
| **updated_at** | **Time** |  |  |
| **account_id** | **String** |  |  |
| **name** | **String** |  |  |
| **platform_role** | [**MerchantRole**](MerchantRole.md) |  |  |
| **status** | **String** |  |  |
| **payments_enabled** | **Boolean** |  |  |
| **payouts_enabled** | **Boolean** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

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

