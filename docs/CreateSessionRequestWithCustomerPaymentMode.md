# Komoju::CreateSessionRequestWithCustomerPaymentMode

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **mode** | **String** | In &#x60;customer_payment&#x60; mode, a payment will be created and:  * If &#x60;customer_id&#x60; is omitted, a new customer will be created. * If &#x60;customer_id&#x60; is given, updated payment information will be saved to that customer. |  |
| **return_url** | **String** | Specify the URL where user will be redirected to after they have completed or aborted the session. A &#x60;session_id&#x60; will be appended to this URL as a query parameter. | [optional] |
| **amount** | **Integer** | Amount greater than or equal to 0, in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **email** | **String** | Customer&#39;s email address. | [optional] |
| **expires_in_seconds** | **Integer** | Time in seconds until the session expires after being created.  The default value and upper limit are 86,400 seconds (24 hours). | [optional] |
| **external_customer_id** | **String** | An unique identifier of your customer. If your system has the concept of user accounts, then the ID of the current logged in user would be appropriate. | [optional] |
| **payment_types** | [**Array&lt;PaymentType&gt;**](PaymentType.md) | Specify which payment types are available for this session.  By default, all activated payment methods will be available for the session if this value is omitted. | [optional] |
| **default_locale** | [**Locale**](Locale.md) |  | [optional] |
| **line_items** | [**Array&lt;LineItem&gt;**](LineItem.md) | Specify the line items which will be displayed on the session page. | [optional] |
| **metadata** | **Object** | Store any additional data you want to associate with the session. The object&#39;s keys and values must be strings. Keys have a maximum length of 30 characters. Values have a maximum length of 2000 characters. | [optional] |
| **payment_data** | [**PaymentDataRequest**](PaymentDataRequest.md) |  | [optional] |
| **customer_id** | **String** | If provided, updated payment details will be saved on the customer. | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::CreateSessionRequestWithCustomerPaymentMode.new(
  mode: null,
  return_url: https://example.com/order/complete,
  amount: 1000,
  currency: null,
  email: john@example.com,
  expires_in_seconds: 86400,
  external_customer_id: 12345,
  payment_types: null,
  default_locale: null,
  line_items: null,
  metadata: null,
  payment_data: null,
  customer_id: cust14ur4hvws08idzacf6et8
)
```

