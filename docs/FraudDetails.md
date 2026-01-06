# Komoju::FraudDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **customer_ip** | **String** | Either an IPv4 or IPv6 |  |
| **customer_email** | **String** |  |  |
| **customer_id** | **String** |  |  |
| **browser_language** | **String** |  |  |
| **browser_user_agent** | **String** |  |  |
| **browser_session_id** | **String** |  |  |
| **phone** | **String** |  |  |
| **billing_address** | [**Address**](Address.md) |  |  |
| **shipping_address** | [**Address**](Address.md) |  |  |

## Example

```ruby
require 'komoju-ruby-client'

instance = Komoju::FraudDetails.new(
  customer_ip: null,
  customer_email: null,
  customer_id: null,
  browser_language: null,
  browser_user_agent: null,
  browser_session_id: null,
  phone: null,
  billing_address: null,
  shipping_address: null
)
```

