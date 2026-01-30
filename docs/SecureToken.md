# Komoju::SecureToken

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **created_at** | **Time** |  |  |
| **verification_status** | **String** |  |  |
| **authentication_url** | **String** |  |  |
| **three_ds_auth_result** | [**ThreeDsAuthResult**](ThreeDsAuthResult.md) |  | [optional] |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::SecureToken.new(
  id: null,
  created_at: null,
  verification_status: null,
  authentication_url: null,
  three_ds_auth_result: null
)
```

