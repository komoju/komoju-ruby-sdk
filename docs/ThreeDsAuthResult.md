# Komoju::ThreeDsAuthResult

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **ds_reference_number** | **String** |  |  |
| **acs_reference_number** | **String** |  |  |
| **three_ds_requestor_trans_id** | **String** |  |  |
| **acs_trans_id** | **String** |  |  |
| **ds_trans_id** | **String** |  |  |
| **eci** | **String** |  |  |
| **message_version** | **String** |  |  |
| **authentication_type** | **String** |  |  |
| **authentication_value** | **String** |  |  |
| **trans_status** | **String** |  |  |
| **three_ds_server_trans_id** | **String** |  |  |

## Example

```ruby
require 'komoju-ruby-sdk'

instance = Komoju::ThreeDsAuthResult.new(
  ds_reference_number: null,
  acs_reference_number: null,
  three_ds_requestor_trans_id: null,
  acs_trans_id: null,
  ds_trans_id: null,
  eci: null,
  message_version: null,
  authentication_type: null,
  authentication_value: null,
  trans_status: null,
  three_ds_server_trans_id: null
)
```

