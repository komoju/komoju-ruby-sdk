# Komoju::TokenPaymentDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **type** | **String** | Payment method type for this token (e.g. \&quot;credit_card\&quot;). |  |
| **email** | **String** | Email address associated with this token. | [optional] |
| **phone** | **String** | Phone number associated with this token. | [optional] |
| **given_name** | **String** | Customer&#39;s given name. | [optional] |
| **family_name** | **String** | Customer&#39;s family name. | [optional] |
| **given_name_kana** | **String** | Customer&#39;s given name in katakana. | [optional] |
| **family_name_kana** | **String** | Customer&#39;s family name in katakana. | [optional] |
| **store** | **String** | Convenience store slug selected for this token (e.g. \&quot;seven-eleven\&quot;). | [optional] |

## Example

```ruby
require 'komoju-sdk'

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

