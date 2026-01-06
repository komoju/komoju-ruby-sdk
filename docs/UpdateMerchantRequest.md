# Komoju::UpdateMerchantRequest

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payments_enabled** | **Boolean** |  | [optional] |
| **payouts_enabled** | **Boolean** |  | [optional] |
| **send_payment_instruction_email** | **Boolean** |  | [optional] |
| **send_payment_receipt_email** | **Boolean** |  | [optional] |
| **send_payment_reminder_email** | **Boolean** |  | [optional] |
| **send_payment_capture_email** | **Boolean** |  | [optional] |
| **send_payment_refund_email** | **Boolean** |  | [optional] |
| **expiry_settings** | [**Array&lt;UpdateMerchantRequestExpirySettingsInner&gt;**](UpdateMerchantRequestExpirySettingsInner.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::UpdateMerchantRequest.new(
  payments_enabled: null,
  payouts_enabled: null,
  send_payment_instruction_email: null,
  send_payment_receipt_email: null,
  send_payment_reminder_email: null,
  send_payment_capture_email: null,
  send_payment_refund_email: null,
  expiry_settings: null
)
```

