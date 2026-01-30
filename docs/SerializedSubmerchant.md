# Komoju::SerializedSubmerchant

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
| **send_payment_instruction_email** | **Boolean** |  |  |
| **send_payment_receipt_email** | **Boolean** |  |  |
| **send_payment_reminder_email** | **Boolean** |  |  |
| **send_payment_refund_email** | **Boolean** |  |  |
| **expiry_settings** | [**Array&lt;SerializedSubmerchantExpirySettingsInner&gt;**](SerializedSubmerchantExpirySettingsInner.md) |  |  |
| **active_payment_methods** | [**Array&lt;SerializedSubmerchantActivePaymentMethodsInner&gt;**](SerializedSubmerchantActivePaymentMethodsInner.md) |  |  |
| **publishable_key** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SerializedSubmerchant.new(
  id: null,
  live: null,
  created_at: null,
  updated_at: null,
  account_id: null,
  name: null,
  platform_role: null,
  status: null,
  payments_enabled: null,
  payouts_enabled: null,
  send_payment_instruction_email: null,
  send_payment_receipt_email: null,
  send_payment_reminder_email: null,
  send_payment_refund_email: null,
  expiry_settings: null,
  active_payment_methods: null,
  publishable_key: null
)
```

