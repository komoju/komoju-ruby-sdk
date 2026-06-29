# Komoju::SerializedSubmerchant

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
| **status** | **String** | Current account/application status of the merchant. |  |
| **payments_enabled** | **Boolean** | Whether payments are currently enabled for this merchant. |  |
| **payouts_enabled** | **Boolean** | Whether payouts are currently enabled for this merchant. |  |
| **send_payment_instruction_email** | **Boolean** | Whether payment instruction emails are sent to customers for this merchant. Omitted for &#x60;payout&#x60;-role merchants. | [optional] |
| **send_payment_receipt_email** | **Boolean** | Whether payment receipt emails are sent to customers for this merchant. Omitted for &#x60;payout&#x60;-role merchants. | [optional] |
| **send_payment_reminder_email** | **Boolean** | Whether payment reminder emails are sent to customers for this merchant. Omitted for &#x60;payout&#x60;-role merchants. | [optional] |
| **send_payment_refund_email** | **Boolean** | Whether refund notification emails are sent to customers for this merchant. Omitted for &#x60;payout&#x60;-role merchants. | [optional] |
| **expiry_settings** | [**Array&lt;SerializedSubmerchantExpirySettingsInner&gt;**](SerializedSubmerchantExpirySettingsInner.md) |  |  |
| **active_payment_methods** | [**Array&lt;SerializedSubmerchantActivePaymentMethodsInner&gt;**](SerializedSubmerchantActivePaymentMethodsInner.md) |  |  |
| **publishable_key** | **String** | The merchant&#39;s publishable API key for client-side use. |  |

## Example

```ruby
require 'komoju-sdk'

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

