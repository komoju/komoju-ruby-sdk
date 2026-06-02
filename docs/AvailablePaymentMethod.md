# Komoju::AvailablePaymentMethod

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **name_en** | **String** | English display name of the payment method. |  |
| **name_ja** | **String** | Japanese display name of the payment method. |  |
| **name_ko** | **String** | Korean display name of the payment method. |  |
| **type_slug** | **String** | Machine-readable type identifier for the payment method. |  |
| **currency** | **String** | Currency this payment method supports. |  |
| **subtypes** | **Array&lt;String&gt;** | Optional list of subtypes or variants (e.g. card brands). | [optional] |
| **secure_token_supported** | **Array&lt;String&gt;** | Optional list of secure token / 3DS flows supported by this payment method. | [optional] |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::AvailablePaymentMethod.new(
  name_en: null,
  name_ja: null,
  name_ko: null,
  type_slug: null,
  currency: null,
  subtypes: null,
  secure_token_supported: null
)
```

