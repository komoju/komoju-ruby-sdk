# Komoju::SharedDetails

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **payments** | [**SharedDetailsPayments**](SharedDetailsPayments.md) |  |  |
| **refunds** | [**SharedDetailsRefunds**](SharedDetailsRefunds.md) |  |  |
| **platform_model** | [**SharedDetailsPlatformModel**](SharedDetailsPlatformModel.md) |  | [optional] |
| **corrections** | [**SharedDetailsCorrections**](SharedDetailsCorrections.md) |  |  |
| **komoju_card_charges** | [**SharedDetailsCorrections**](SharedDetailsCorrections.md) |  |  |
| **disbursements** | [**SharedDetailsDisbursements**](SharedDetailsDisbursements.md) |  |  |
| **misc** | [**SharedDetailsMisc**](SharedDetailsMisc.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::SharedDetails.new(
  payments: null,
  refunds: null,
  platform_model: null,
  corrections: null,
  komoju_card_charges: null,
  disbursements: null,
  misc: null
)
```

