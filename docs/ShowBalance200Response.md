# Komoju::ShowBalance200Response

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **currency** | [**Currency**](Currency.md) |  |  |
| **total_balance_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
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

instance = Komoju::ShowBalance200Response.new(
  currency: null,
  total_balance_cents: null,
  payments: null,
  refunds: null,
  platform_model: null,
  corrections: null,
  komoju_card_charges: null,
  disbursements: null,
  misc: null
)
```

