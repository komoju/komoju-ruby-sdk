# Komoju::TokenPaymentDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type for this token (e.g. \&quot;credit_card\&quot;). |  |
| **email** | **String** | Email address associated with this token. |  |
| **phone** | **String** | Phone number associated with this token. |  |
| **given_name** | **String** | Customer&#39;s given name. |  |
| **family_name** | **String** | Customer&#39;s family name. |  |
| **given_name_kana** | **String** | Customer&#39;s given name in katakana. |  |
| **family_name_kana** | **String** | Customer&#39;s family name in katakana. |  |
| **store** | **String** | Convenience store slug selected for this token (e.g. \&quot;seven-eleven\&quot;). |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::TokenPaymentDetails.new(
  type: null,
  email: null,
  phone: null,
  given_name: null,
  family_name: null,
  given_name_kana: null,
  family_name_kana: null,
  store: null
)
```

