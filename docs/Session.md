# Komoju::Session

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;session\&quot;. |  |
| **mode** | [**SessionMode**](SessionMode.md) |  |  |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **session_url** | **String** | URL to redirect the customer to for completing the session. |  |
| **return_url** | **String** | URL the customer is redirected to after completing or cancelling the session. |  |
| **default_locale** | [**Locale**](Locale.md) |  |  |
| **payment_methods** | [**Array&lt;PaymentMethod&gt;**](PaymentMethod.md) | List of payment methods available for this session. |  |
| **created_at** | **Time** | Timestamp when the session was created. |  |
| **cancelled_at** | **Time** | Timestamp when the session was cancelled, or null if not cancelled. |  |
| **completed_at** | **Time** | Timestamp when the session was completed, or null if not completed. |  |
| **status** | [**SessionStatus**](SessionStatus.md) |  |  |
| **expired** | **Boolean** | Whether the session has expired. |  |
| **merchant** | [**MerchantData**](MerchantData.md) |  |  |
| **metadata** | **Object** | Arbitrary key-value metadata attached to this session at creation time. |  |
| **payment** | [**Payment**](Payment.md) |  |  |
| **payment_data** | [**PaymentData**](PaymentData.md) |  | [optional] |
| **customer_id** | **String** | ID of the customer associated with this session, if any. | [optional] |
| **secure_token** | **String** | Secure token for client-side session access. | [optional] |
| **line_items** | [**Array&lt;LineItem&gt;**](LineItem.md) | Line items attached to this session. | [optional] |
| **merchant_id** | **String** | ID of the merchant associated with this session. | [optional] |
| **email** | **String** | Customer email address associated with this session. | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::Session.new(
  id: null,
  resource: null,
  mode: null,
  amount: null,
  currency: null,
  session_url: null,
  return_url: null,
  default_locale: null,
  payment_methods: null,
  created_at: null,
  cancelled_at: null,
  completed_at: null,
  status: null,
  expired: null,
  merchant: null,
  metadata: null,
  payment: null,
  payment_data: null,
  customer_id: null,
  secure_token: null,
  line_items: null,
  merchant_id: null,
  email: null
)
```

