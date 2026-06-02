# Komoju::FraudDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_ip** | **String** | IPv4 or IPv6-formatted IP address of the customer at the time of payment. |  |
| **customer_email** | **String** | Customer&#39;s email address.  This field can be omitted if &#x60;email&#x60; is provided in &#x60;email&#x60; field inside &#x60;payment_details&#x60; of create payment request, or in the create payment session request. Otherwise, this field is required. |  |
| **customer_id** | **String** | An unique identifier of your customer. If your system has the concept of user accounts, then the ID of the current logged in user would be appropriate. | [optional] |
| **browser_language** | **String** | Customer&#39;s current language setting. | [optional] |
| **browser_user_agent** | **String** | Browser&#39;s [User-Agent](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/User-Agent) string. | [optional] |
| **browser_session_id** | **String** | A unique identifier for the current browser session. We expect this to behave similarly to the lifetime of [window.sessionStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage) in a web browsing context. | [optional] |
| **phone** | **String** | Customer&#39;s phone number. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::FraudDetails.new(
  customer_ip: ::1,
  customer_email: john@example.com,
  customer_id: 123,
  browser_language: ja-JP,
  browser_user_agent: Mozilla/5.0 (Macintosh; Intel Mac OS X x.y; rv:42.0) Gecko/20100101 Firefox/42.0,
  browser_session_id: abc1234,
  phone: 07012345678
)
```

