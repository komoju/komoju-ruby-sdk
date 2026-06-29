# Komoju::Settlement

## Properties

| Name | Type | Description | Notes |
| ---- | ---- | ----------- | ----- |
| **id** | **String** | A unique 25-character alphanumeric resource identifier. |  |
| **resource** | **String** | Resource type name, always \&quot;settlement\&quot;. |  |
| **reference** | **String** | Human-readable reference code for this settlement. |  |
| **status** | [**Status**](Status.md) |  |  |
| **merchant_name** | **String** | Name of the merchant associated with this settlement. |  |
| **company_name** | **String** | Legal company name of the merchant, or null if not set. |  |
| **cycle** | **String** | Settlement cycle identifier (e.g. the week or month period covered). |  |
| **transaction_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **currency** | [**Currency**](Currency.md) |  |  |
| **fee_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **fee_tax_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **settlement_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **fx_currency** | [**Currency**](Currency.md) |  |  |
| **fx_conversion_rate** | **String** | Exchange rate applied for FX conversion. |  |
| **fx_conversion_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **bank_transfer_fee_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **remittance_amount_cents** | **Integer** | Amount in the lowest denomination of the currency (e.g. cents for USD). |  |
| **cutoff_time** | **Time** | Cutoff timestamp for transactions included in this settlement. |  |
| **created_at** | **Time** | Timestamp when this settlement record was created. |  |
| **download** | [**SettlementDownload**](SettlementDownload.md) |  |  |

## Example

```ruby
require 'komoju-sdk'

instance = Komoju::Settlement.new(
  id: null,
  resource: null,
  reference: null,
  status: null,
  merchant_name: null,
  company_name: null,
  cycle: null,
  transaction_amount_cents: null,
  currency: null,
  fee_amount_cents: null,
  fee_tax_amount_cents: null,
  settlement_amount_cents: null,
  fx_currency: null,
  fx_conversion_rate: null,
  fx_conversion_amount_cents: null,
  bank_transfer_fee_amount_cents: null,
  remittance_amount_cents: null,
  cutoff_time: null,
  created_at: null,
  download: null
)
```

